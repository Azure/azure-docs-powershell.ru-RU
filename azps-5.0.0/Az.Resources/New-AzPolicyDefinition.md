---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 31F2AF24-488D-4CAF-A9C8-C8DAE76E031F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyDefinition.md
ms.openlocfilehash: 51c5608c8212b519e6ca979e470c2ab1a5d96e6b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94315689"
---
# <span data-ttu-id="de226-101">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="de226-101">New-AzPolicyDefinition</span></span>

## <span data-ttu-id="de226-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="de226-102">SYNOPSIS</span></span>
<span data-ttu-id="de226-103">Создание определения политики.</span><span class="sxs-lookup"><span data-stu-id="de226-103">Creates a policy definition.</span></span>

## <span data-ttu-id="de226-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="de226-104">SYNTAX</span></span>

### <span data-ttu-id="de226-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="de226-105">NameParameterSet (Default)</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de226-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="de226-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de226-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="de226-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de226-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="de226-108">DESCRIPTION</span></span>
<span data-ttu-id="de226-109">Командлет **New-AzPolicyDefinition** создает определение политики, включающее правило политики в формате JavaScript Object Notation (JSON).</span><span class="sxs-lookup"><span data-stu-id="de226-109">The **New-AzPolicyDefinition** cmdlet creates a policy definition that includes a policy rule in JavaScript Object Notation (JSON) format.</span></span>

## <span data-ttu-id="de226-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="de226-110">EXAMPLES</span></span>

### <span data-ttu-id="de226-111">Пример 1: Создание определения политики с помощью файла политики</span><span class="sxs-lookup"><span data-stu-id="de226-111">Example 1: Create a policy definition by using a policy file</span></span>
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
PS C:\> New-AzPolicyDefinition -Name 'LocationDefinition' -Policy C:\LocationPolicy.json
```

<span data-ttu-id="de226-112">Эта команда создает определение политики с именем LocationDefinition, которое включает правило политики, указанное в C:\LocationPolicy.json.</span><span class="sxs-lookup"><span data-stu-id="de226-112">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="de226-113">Пример содержимого для LocationPolicy.jsфайла приведен выше.</span><span class="sxs-lookup"><span data-stu-id="de226-113">Example content for the LocationPolicy.json file is provided above.</span></span>

### <span data-ttu-id="de226-114">Пример 2: Создание определения параметризованной политики с помощью встроенных параметров</span><span class="sxs-lookup"><span data-stu-id="de226-114">Example 2: Create a parameterized policy definition using inline parameters</span></span>
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
PS C:\> New-AzPolicyDefinition -Name 'LocationDefinition' -Policy C:\LocationPolicy.json -Parameter '{ "listOfAllowedLocations": { "type": "array" } }'
```

<span data-ttu-id="de226-115">Эта команда создает определение политики с именем LocationDefinition, которое включает правило политики, указанное в C:\LocationPolicy.json.</span><span class="sxs-lookup"><span data-stu-id="de226-115">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="de226-116">Определение параметра для правила политики предоставляется внутри строки.</span><span class="sxs-lookup"><span data-stu-id="de226-116">The parameter definition for the policy rule is provided inline.</span></span>

### <span data-ttu-id="de226-117">Пример 3: Создание определения политики в строке группы управления</span><span class="sxs-lookup"><span data-stu-id="de226-117">Example 3: Create a policy definition inline in a management group</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName Dept42 -DisplayName 'Virtual Machine policy definition' -Policy '{"if":{"field":"type","equals":"Microsoft.Compute/virtualMachines"},"then":{"effect":"deny"}}'
```

<span data-ttu-id="de226-118">Эта команда создает определение политики с именем VMPolicyDefinition в группе управления Dept42.</span><span class="sxs-lookup"><span data-stu-id="de226-118">This command creates a policy definition named VMPolicyDefinition in management group Dept42.</span></span>
<span data-ttu-id="de226-119">Команда задает политику в виде строки в допустимом формате JSON.</span><span class="sxs-lookup"><span data-stu-id="de226-119">The command specifies the policy as a string in valid JSON format.</span></span>

### <span data-ttu-id="de226-120">Пример 4: Создание определения политики в строке с метаданными</span><span class="sxs-lookup"><span data-stu-id="de226-120">Example 4: Create a policy definition inline with metadata</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'VMPolicyDefinition' -Metadata '{"category":"Virtual Machine"}' -Policy '{"if":{"field":"type","equals":"Microsoft.Compute/virtualMachines"},"then":{"effect":"deny"}}'


Name               : VMPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
ResourceName       : VMPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=VMPolicyDefinition; policyType=Custom; mode=All; metadata=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
```

<span data-ttu-id="de226-121">Эта команда создает определение политики с именем VMPolicyDefinition и метаданные, указывающие на категорию "виртуальная машина".</span><span class="sxs-lookup"><span data-stu-id="de226-121">This command creates a policy definition named VMPolicyDefinition with metadata indicating its category is "Virtual Machine".</span></span>
<span data-ttu-id="de226-122">Команда задает политику в виде строки в допустимом формате JSON.</span><span class="sxs-lookup"><span data-stu-id="de226-122">The command specifies the policy as a string in valid JSON format.</span></span>

### <span data-ttu-id="de226-123">Пример 5: Создание определения политики в строке "режим"</span><span class="sxs-lookup"><span data-stu-id="de226-123">Example 5: Create a policy definition inline with mode</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'TagsPolicyDefinition' -Policy '{"if":{"value":"[less(length(field(''tags'')), 3)]","equals":true},"then":{"effect":"deny"}}' -Mode Indexed


Name               : TagsPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/TagsPolicyDefinition
ResourceName       : TagsPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=TagsPolicyDefinition; policyType=Custom; mode=Indexed; metadata=; parameters=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/TagsPolicyDefinition
```

<span data-ttu-id="de226-124">Эта команда создает определение политики с именем TagsPolicyDefinition с режимом "indexed", которое указывает, что политика должна оцениваться только для типов ресурсов, поддерживающих Теги и расположение.</span><span class="sxs-lookup"><span data-stu-id="de226-124">This command creates a policy definition named TagsPolicyDefinition with mode "Indexed" indicating the policy should be evaluated only for resource types that support tags and location.</span></span>

## <span data-ttu-id="de226-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="de226-125">PARAMETERS</span></span>

### <span data-ttu-id="de226-126">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="de226-126">-ApiVersion</span></span>
<span data-ttu-id="de226-127">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="de226-127">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="de226-128">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="de226-128">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="de226-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de226-129">-DefaultProfile</span></span>
<span data-ttu-id="de226-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="de226-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="de226-131">-Описание</span><span class="sxs-lookup"><span data-stu-id="de226-131">-Description</span></span>
<span data-ttu-id="de226-132">Задает описание определения политики.</span><span class="sxs-lookup"><span data-stu-id="de226-132">Specifies a description for the policy definition.</span></span>

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

### <span data-ttu-id="de226-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="de226-133">-DisplayName</span></span>
<span data-ttu-id="de226-134">Задает отображаемое имя для определения политики.</span><span class="sxs-lookup"><span data-stu-id="de226-134">Specifies a display name for the policy definition.</span></span>

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

### <span data-ttu-id="de226-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="de226-135">-ManagementGroupName</span></span>
<span data-ttu-id="de226-136">Имя группы управления для нового определения политики.</span><span class="sxs-lookup"><span data-stu-id="de226-136">The name of the management group of the new policy definition.</span></span>

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

### <span data-ttu-id="de226-137">-Metadata</span><span class="sxs-lookup"><span data-stu-id="de226-137">-Metadata</span></span>
<span data-ttu-id="de226-138">Метаданные для определения политики.</span><span class="sxs-lookup"><span data-stu-id="de226-138">The metadata for policy definition.</span></span> <span data-ttu-id="de226-139">Это может быть путь к имени файла, содержащему метаданные, или метаданным в виде строки.</span><span class="sxs-lookup"><span data-stu-id="de226-139">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="de226-140">Режим</span><span class="sxs-lookup"><span data-stu-id="de226-140">-Mode</span></span>
<span data-ttu-id="de226-141">Режим определения политики</span><span class="sxs-lookup"><span data-stu-id="de226-141">The mode of the policy definition</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: All
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de226-142">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="de226-142">-Name</span></span>
<span data-ttu-id="de226-143">Задает имя для определения политики.</span><span class="sxs-lookup"><span data-stu-id="de226-143">Specifies a name for the policy definition.</span></span>

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

### <span data-ttu-id="de226-144">-Параметр</span><span class="sxs-lookup"><span data-stu-id="de226-144">-Parameter</span></span>
<span data-ttu-id="de226-145">Объявление параметров для определения политики.</span><span class="sxs-lookup"><span data-stu-id="de226-145">The parameters declaration for policy definition.</span></span> <span data-ttu-id="de226-146">Это может быть путь к имени файла, в котором содержится объявление параметров, или объявление параметров как String.</span><span class="sxs-lookup"><span data-stu-id="de226-146">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="de226-147">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="de226-147">-Policy</span></span>
<span data-ttu-id="de226-148">Определяет правило политики для определения политики.</span><span class="sxs-lookup"><span data-stu-id="de226-148">Specifies a policy rule for the policy definition.</span></span>
<span data-ttu-id="de226-149">Вы можете указать путь к JSON-файлу или строку, содержащую политику в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="de226-149">You can specify the path of a .json file or a string that contains the policy in JSON format.</span></span>

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

### <span data-ttu-id="de226-150">-Pre</span><span class="sxs-lookup"><span data-stu-id="de226-150">-Pre</span></span>
<span data-ttu-id="de226-151">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="de226-151">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="de226-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="de226-152">-SubscriptionId</span></span>
<span data-ttu-id="de226-153">Идентификатор подписки нового определения политики.</span><span class="sxs-lookup"><span data-stu-id="de226-153">The subscription ID of the new policy definition.</span></span>

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

### <span data-ttu-id="de226-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de226-154">CommonParameters</span></span>
<span data-ttu-id="de226-155">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="de226-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de226-156">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de226-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de226-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="de226-157">INPUTS</span></span>

### <span data-ttu-id="de226-158">System. String</span><span class="sxs-lookup"><span data-stu-id="de226-158">System.String</span></span>

### <span data-ttu-id="de226-159">System. Nullable "1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="de226-159">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="de226-160">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="de226-160">OUTPUTS</span></span>

### <span data-ttu-id="de226-161">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="de226-161">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="de226-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="de226-162">NOTES</span></span>

## <span data-ttu-id="de226-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="de226-163">RELATED LINKS</span></span>

[<span data-ttu-id="de226-164">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="de226-164">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="de226-165">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="de226-165">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

[<span data-ttu-id="de226-166">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="de226-166">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


