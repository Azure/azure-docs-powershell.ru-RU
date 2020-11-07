---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 31F2AF24-488D-4CAF-A9C8-C8DAE76E031F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyDefinition.md
ms.openlocfilehash: 22c8ea5c93a301796b2b42184a54744e9841163d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93731955"
---
# <span data-ttu-id="b932c-101">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b932c-101">New-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="b932c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b932c-102">SYNOPSIS</span></span>
<span data-ttu-id="b932c-103">Создание определения политики.</span><span class="sxs-lookup"><span data-stu-id="b932c-103">Creates a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b932c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b932c-104">SYNTAX</span></span>

### <span data-ttu-id="b932c-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b932c-105">NameParameterSet (Default)</span></span>
```
New-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b932c-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b932c-106">ManagementGroupNameParameterSet</span></span>
```
New-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b932c-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b932c-107">SubscriptionIdParameterSet</span></span>
```
New-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b932c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b932c-108">DESCRIPTION</span></span>
<span data-ttu-id="b932c-109">Командлет **New-AzureRmPolicyDefinition** создает определение политики, включающее правило политики в формате JavaScript Object Notation (JSON).</span><span class="sxs-lookup"><span data-stu-id="b932c-109">The **New-AzureRmPolicyDefinition** cmdlet creates a policy definition that includes a policy rule in JavaScript Object Notation (JSON) format.</span></span>

## <span data-ttu-id="b932c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b932c-110">EXAMPLES</span></span>

### <span data-ttu-id="b932c-111">Пример 1: Создание определения политики с помощью файла политики</span><span class="sxs-lookup"><span data-stu-id="b932c-111">Example 1: Create a policy definition by using a policy file</span></span>
```
{
   "if": {
      "field": "location",
      "notIn": ["eastus", "westus", "centralus"]
   },
   "then": {
      "effect": "audit"
   }
}
```

```
PS C:\> New-AzureRmPolicyDefinition -Name 'LocationDefinition' -Policy C:\LocationPolicy.json
```

<span data-ttu-id="b932c-112">Эта команда создает определение политики с именем LocationDefinition, которое включает правило политики, указанное в C:\LocationPolicy.json.</span><span class="sxs-lookup"><span data-stu-id="b932c-112">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="b932c-113">Пример содержимого для LocationPolicy.jsфайла приведен выше.</span><span class="sxs-lookup"><span data-stu-id="b932c-113">Example content for the LocationPolicy.json file is provided above.</span></span>

### <span data-ttu-id="b932c-114">Пример 2: Создание определения параметризованной политики с помощью встроенных параметров</span><span class="sxs-lookup"><span data-stu-id="b932c-114">Example 2: Create a parameterized policy definition using inline parameters</span></span>
```
{
   "if": {
      "field": "location",
      "notIn": "[parameters('listOfAllowedLocations')]"
   },
   "then": {
      "effect": "audit"
   }
}
```

```
PS C:\> New-AzureRmPolicyDefinition -Name 'LocationDefinition' -Policy C:\LocationPolicy.json -Parameter '{ "listOfAllowedLocations": { "type": "array" } }'
```

<span data-ttu-id="b932c-115">Эта команда создает определение политики с именем LocationDefinition, которое включает правило политики, указанное в C:\LocationPolicy.json.</span><span class="sxs-lookup"><span data-stu-id="b932c-115">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="b932c-116">Определение параметра для правила политики предоставляется внутри строки.</span><span class="sxs-lookup"><span data-stu-id="b932c-116">The parameter definition for the policy rule is provided inline.</span></span>

### <span data-ttu-id="b932c-117">Пример 3: Создание определения политики в строке группы управления</span><span class="sxs-lookup"><span data-stu-id="b932c-117">Example 3: Create a policy definition inline in a management group</span></span>
```
PS C:\> New-AzureRmPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName Dept42 -DisplayName 'Virtual Machine policy definition' -Policy '{"if":{"source":"action","equals":"Microsoft.Compute/virtualMachines/write"},"then":{"effect":"deny"}}'
```

<span data-ttu-id="b932c-118">Эта команда создает определение политики с именем VMPolicyDefinition в группе управления Dept42.</span><span class="sxs-lookup"><span data-stu-id="b932c-118">This command creates a policy definition named VMPolicyDefinition in management group Dept42.</span></span>
<span data-ttu-id="b932c-119">Команда задает политику в виде строки в допустимом формате JSON.</span><span class="sxs-lookup"><span data-stu-id="b932c-119">The command specifies the policy as a string in valid JSON format.</span></span>

### <span data-ttu-id="b932c-120">Пример 4: Создание определения политики в строке с метаданными</span><span class="sxs-lookup"><span data-stu-id="b932c-120">Example 4: Create a policy definition inline with metadata</span></span>
```
PS C:\> New-AzureRmPolicyDefinition -Name 'VMPolicyDefinition' -Metadata '{"Category":"Virtual Machine"}' -Policy '{"if":{"source":"action","equals":"Microsoft.Compute/virtualMachines/write"},"then":{"effect":"deny"}}'


Name               : VMPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
ResourceName       : VMPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=VMPolicyDefinition; policyType=Custom; mode=All; metadata=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
```

<span data-ttu-id="b932c-121">Эта команда создает определение политики с именем VMPolicyDefinition и метаданные, указывающие на категорию "виртуальная машина".</span><span class="sxs-lookup"><span data-stu-id="b932c-121">This command creates a policy definition named VMPolicyDefinition with metadata indicating its category is "Virtual Machine".</span></span>
<span data-ttu-id="b932c-122">Команда задает политику в виде строки в допустимом формате JSON.</span><span class="sxs-lookup"><span data-stu-id="b932c-122">The command specifies the policy as a string in valid JSON format.</span></span>

## <span data-ttu-id="b932c-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b932c-123">PARAMETERS</span></span>

### <span data-ttu-id="b932c-124">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b932c-124">-ApiVersion</span></span>
<span data-ttu-id="b932c-125">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b932c-125">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="b932c-126">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="b932c-126">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="b932c-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b932c-127">-DefaultProfile</span></span>
<span data-ttu-id="b932c-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b932c-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b932c-129">-Описание</span><span class="sxs-lookup"><span data-stu-id="b932c-129">-Description</span></span>
<span data-ttu-id="b932c-130">Задает описание определения политики.</span><span class="sxs-lookup"><span data-stu-id="b932c-130">Specifies a description for the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b932c-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b932c-131">-DisplayName</span></span>
<span data-ttu-id="b932c-132">Задает отображаемое имя для определения политики.</span><span class="sxs-lookup"><span data-stu-id="b932c-132">Specifies a display name for the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b932c-133">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b932c-133">-InformationAction</span></span>
<span data-ttu-id="b932c-134">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="b932c-134">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="b932c-135">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b932c-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b932c-136">Продолжал</span><span class="sxs-lookup"><span data-stu-id="b932c-136">Continue</span></span>
- <span data-ttu-id="b932c-137">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="b932c-137">Ignore</span></span>
- <span data-ttu-id="b932c-138">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="b932c-138">Inquire</span></span>
- <span data-ttu-id="b932c-139">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b932c-139">SilentlyContinue</span></span>
- <span data-ttu-id="b932c-140">Остановить</span><span class="sxs-lookup"><span data-stu-id="b932c-140">Stop</span></span>
- <span data-ttu-id="b932c-141">Рвать</span><span class="sxs-lookup"><span data-stu-id="b932c-141">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b932c-142">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b932c-142">-InformationVariable</span></span>
<span data-ttu-id="b932c-143">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="b932c-143">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b932c-144">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="b932c-144">-ManagementGroupName</span></span>
<span data-ttu-id="b932c-145">Имя группы управления для нового определения политики.</span><span class="sxs-lookup"><span data-stu-id="b932c-145">The name of the management group of the new policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b932c-146">-Metadata</span><span class="sxs-lookup"><span data-stu-id="b932c-146">-Metadata</span></span>
<span data-ttu-id="b932c-147">Метаданные для определения политики.</span><span class="sxs-lookup"><span data-stu-id="b932c-147">The metadata for policy definition.</span></span> <span data-ttu-id="b932c-148">Это может быть путь к имени файла, содержащему метаданные, или метаданным в виде строки.</span><span class="sxs-lookup"><span data-stu-id="b932c-148">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b932c-149">Режим</span><span class="sxs-lookup"><span data-stu-id="b932c-149">-Mode</span></span>
<span data-ttu-id="b932c-150">Режим определения политики</span><span class="sxs-lookup"><span data-stu-id="b932c-150">The mode of the policy definition</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Policy.PolicyDefinitionMode]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b932c-151">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b932c-151">-Name</span></span>
<span data-ttu-id="b932c-152">Задает имя для определения политики.</span><span class="sxs-lookup"><span data-stu-id="b932c-152">Specifies a name for the policy definition.</span></span>

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

### <span data-ttu-id="b932c-153">-Параметр</span><span class="sxs-lookup"><span data-stu-id="b932c-153">-Parameter</span></span>
<span data-ttu-id="b932c-154">Объявление параметров для определения политики.</span><span class="sxs-lookup"><span data-stu-id="b932c-154">The parameters declaration for policy definition.</span></span> <span data-ttu-id="b932c-155">Это может быть путь к имени файла, в котором содержится объявление параметров, или объявление параметров как String.</span><span class="sxs-lookup"><span data-stu-id="b932c-155">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b932c-156">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="b932c-156">-Policy</span></span>
<span data-ttu-id="b932c-157">Определяет правило политики для определения политики.</span><span class="sxs-lookup"><span data-stu-id="b932c-157">Specifies a policy rule for the policy definition.</span></span>
<span data-ttu-id="b932c-158">Вы можете указать путь к JSON-файлу или строку, содержащую политику в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="b932c-158">You can specify the path of a .json file or a string that contains the policy in JSON format.</span></span>

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

### <span data-ttu-id="b932c-159">-Pre</span><span class="sxs-lookup"><span data-stu-id="b932c-159">-Pre</span></span>
<span data-ttu-id="b932c-160">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="b932c-160">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b932c-161">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b932c-161">-SubscriptionId</span></span>
<span data-ttu-id="b932c-162">Идентификатор подписки нового определения политики.</span><span class="sxs-lookup"><span data-stu-id="b932c-162">The subscription ID of the new policy definition.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b932c-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b932c-163">CommonParameters</span></span>
<span data-ttu-id="b932c-164">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b932c-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b932c-165">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b932c-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b932c-166">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b932c-166">INPUTS</span></span>

## <span data-ttu-id="b932c-167">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b932c-167">OUTPUTS</span></span>

## <span data-ttu-id="b932c-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="b932c-168">NOTES</span></span>

## <span data-ttu-id="b932c-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b932c-169">RELATED LINKS</span></span>

[<span data-ttu-id="b932c-170">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b932c-170">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="b932c-171">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b932c-171">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="b932c-172">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b932c-172">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


