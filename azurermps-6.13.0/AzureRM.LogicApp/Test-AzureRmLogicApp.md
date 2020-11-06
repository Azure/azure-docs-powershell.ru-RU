---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 929F4593-2A71-49B9-87F8-F24FA9F6E314
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/test-azurermlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Test-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Test-AzureRmLogicApp.md
ms.openlocfilehash: 35ce8352670aa2af2a7051736e1b986b83bcc64b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565402"
---
# <span data-ttu-id="e677e-101">Test-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="e677e-101">Test-AzureRmLogicApp</span></span>

## <span data-ttu-id="e677e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e677e-102">SYNOPSIS</span></span>
<span data-ttu-id="e677e-103">Проверка определения логического приложения.</span><span class="sxs-lookup"><span data-stu-id="e677e-103">Validates a logic app definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e677e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e677e-104">SYNTAX</span></span>

### <span data-ttu-id="e677e-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="e677e-105">LogicAppWithDefinitionParameterSet</span></span>
```
Test-AzureRmLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-Definition <Object>] [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e677e-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="e677e-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
Test-AzureRmLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e677e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e677e-107">DESCRIPTION</span></span>
<span data-ttu-id="e677e-108">Командлет **Test-AzureRmLogicApp** проверяет определение приложения логики в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e677e-108">The **Test-AzureRmLogicApp** cmdlet validates a logic app definition in a resource group.</span></span>
<span data-ttu-id="e677e-109">Укажите имя логики приложения, имя группы ресурсов, расположение, состояние, идентификатор учетной записи для интеграции или параметры.</span><span class="sxs-lookup"><span data-stu-id="e677e-109">Specify the logic app name, resource group name, location, state, integration account ID, or parameters.</span></span>
<span data-ttu-id="e677e-110">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="e677e-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="e677e-111">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="e677e-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="e677e-112">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="e677e-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="e677e-113">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="e677e-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="e677e-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e677e-114">EXAMPLES</span></span>

### <span data-ttu-id="e677e-115">Пример 1: проверка логического приложения с помощью путей к файлам</span><span class="sxs-lookup"><span data-stu-id="e677e-115">Example 1: Validate a logic app by using file paths</span></span>
```
PS C:\>Test-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -DefinitionFilePath "d:\workflows\Definition.json" -ParameterFilePath "d:\workflows\Parameters.json"
```

<span data-ttu-id="e677e-116">Эта команда проверяет логическое приложение с именем LogicApp01 в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e677e-116">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="e677e-117">Команда задает пути к файлу определения и параметров.</span><span class="sxs-lookup"><span data-stu-id="e677e-117">The command specifies definition and parameter file paths.</span></span>

### <span data-ttu-id="e677e-118">Пример 2: проверка логического приложения с помощью объектов</span><span class="sxs-lookup"><span data-stu-id="e677e-118">Example 2: Validate a logic app by using objects</span></span>
```
PS C:\>Test-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
```

<span data-ttu-id="e677e-119">Эта команда проверяет логическое приложение с именем LogicApp01 в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e677e-119">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="e677e-120">Команда задает определение и объекты параметров.</span><span class="sxs-lookup"><span data-stu-id="e677e-120">The command specifies definition and parameter objects.</span></span>

## <span data-ttu-id="e677e-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e677e-121">PARAMETERS</span></span>

### <span data-ttu-id="e677e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e677e-122">-DefaultProfile</span></span>
<span data-ttu-id="e677e-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e677e-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e677e-124">-Определение</span><span class="sxs-lookup"><span data-stu-id="e677e-124">-Definition</span></span>
<span data-ttu-id="e677e-125">Указывает определение приложения логики в виде объекта или строки в формате JSON (объектной нотации).</span><span class="sxs-lookup"><span data-stu-id="e677e-125">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="e677e-126">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="e677e-126">-DefinitionFilePath</span></span>
<span data-ttu-id="e677e-127">Задает определение приложения логики в качестве пути к файлу определения в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="e677e-127">Specifies the definition of your logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="e677e-128">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="e677e-128">-IntegrationAccountId</span></span>
<span data-ttu-id="e677e-129">Указывает идентификатор учетной записи интеграции для приложения логики.</span><span class="sxs-lookup"><span data-stu-id="e677e-129">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="e677e-130">-Location</span><span class="sxs-lookup"><span data-stu-id="e677e-130">-Location</span></span>
<span data-ttu-id="e677e-131">Указывает расположение приложения логики.</span><span class="sxs-lookup"><span data-stu-id="e677e-131">Specifies the location of the logic app.</span></span>
<span data-ttu-id="e677e-132">Введите расположение центра обработки данных Azure, например Западная часть США или Юго-Восток Азии.</span><span class="sxs-lookup"><span data-stu-id="e677e-132">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="e677e-133">Вы можете поместить логику приложения в любое место.</span><span class="sxs-lookup"><span data-stu-id="e677e-133">You can place a logic app in any location.</span></span>

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

### <span data-ttu-id="e677e-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e677e-134">-Name</span></span>
<span data-ttu-id="e677e-135">Указывает имя приложения логики.</span><span class="sxs-lookup"><span data-stu-id="e677e-135">Specifies the name of the logic app.</span></span>

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

### <span data-ttu-id="e677e-136">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="e677e-136">-ParameterFilePath</span></span>
<span data-ttu-id="e677e-137">Задает путь к файлу форматированного параметра JSON.</span><span class="sxs-lookup"><span data-stu-id="e677e-137">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="e677e-138">-Parameters</span><span class="sxs-lookup"><span data-stu-id="e677e-138">-Parameters</span></span>
<span data-ttu-id="e677e-139">Указывает объект коллекции Parameters для приложения логики.</span><span class="sxs-lookup"><span data-stu-id="e677e-139">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="e677e-140">Укажите хэш-таблицу, словарь \<string\> или словарь \<string, WorkflowParameter\> .</span><span class="sxs-lookup"><span data-stu-id="e677e-140">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="e677e-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e677e-141">-ResourceGroupName</span></span>
<span data-ttu-id="e677e-142">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e677e-142">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e677e-143">-State</span><span class="sxs-lookup"><span data-stu-id="e677e-143">-State</span></span>
<span data-ttu-id="e677e-144">Задает состояние приложения логики.</span><span class="sxs-lookup"><span data-stu-id="e677e-144">Specifies a state of the logic app.</span></span>
<span data-ttu-id="e677e-145">Допустимые значения этого параметра: включены и отключены.</span><span class="sxs-lookup"><span data-stu-id="e677e-145">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="e677e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e677e-146">CommonParameters</span></span>
<span data-ttu-id="e677e-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e677e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e677e-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e677e-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e677e-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e677e-149">INPUTS</span></span>

### <span data-ttu-id="e677e-150">System. String</span><span class="sxs-lookup"><span data-stu-id="e677e-150">System.String</span></span>

## <span data-ttu-id="e677e-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e677e-151">OUTPUTS</span></span>

### <span data-ttu-id="e677e-152">System. void</span><span class="sxs-lookup"><span data-stu-id="e677e-152">System.Void</span></span>

## <span data-ttu-id="e677e-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="e677e-153">NOTES</span></span>

## <span data-ttu-id="e677e-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e677e-154">RELATED LINKS</span></span>

[<span data-ttu-id="e677e-155">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="e677e-155">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="e677e-156">New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="e677e-156">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="e677e-157">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="e677e-157">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="e677e-158">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="e677e-158">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="e677e-159">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="e677e-159">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


