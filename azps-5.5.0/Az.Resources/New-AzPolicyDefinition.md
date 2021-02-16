---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 31F2AF24-488D-4CAF-A9C8-C8DAE76E031F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyDefinition.md
ms.openlocfilehash: 51c5608c8212b519e6ca979e470c2ab1a5d96e6b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242517"
---
# <span data-ttu-id="a9bb2-101">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a9bb2-101">New-AzPolicyDefinition</span></span>

## <span data-ttu-id="a9bb2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9bb2-102">SYNOPSIS</span></span>
<span data-ttu-id="a9bb2-103">Создает определение политики.</span><span class="sxs-lookup"><span data-stu-id="a9bb2-103">Creates a policy definition.</span></span>

## <span data-ttu-id="a9bb2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a9bb2-104">SYNTAX</span></span>

### <span data-ttu-id="a9bb2-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a9bb2-105">NameParameterSet (Default)</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9bb2-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9bb2-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9bb2-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9bb2-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9bb2-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a9bb2-108">DESCRIPTION</span></span>
<span data-ttu-id="a9bb2-109">Для **этого создается** определение политики, в которое входит правило политики в формате нотации объектов JavaScript (JSON).</span><span class="sxs-lookup"><span data-stu-id="a9bb2-109">The **New-AzPolicyDefinition** cmdlet creates a policy definition that includes a policy rule in JavaScript Object Notation (JSON) format.</span></span>

## <span data-ttu-id="a9bb2-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a9bb2-110">EXAMPLES</span></span>

### <span data-ttu-id="a9bb2-111">Пример 1. Создание определения политики с помощью файла политики</span><span class="sxs-lookup"><span data-stu-id="a9bb2-111">Example 1: Create a policy definition by using a policy file</span></span>
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

<span data-ttu-id="a9bb2-112">Эта команда создает определение политики LocationDefinition, которое содержит правило политики, указанное в C:\LocationPolicy.js.</span><span class="sxs-lookup"><span data-stu-id="a9bb2-112">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="a9bb2-113">Выше представлен пример LocationPolicy.jsфайла.</span><span class="sxs-lookup"><span data-stu-id="a9bb2-113">Example content for the LocationPolicy.json file is provided above.</span></span>

### <span data-ttu-id="a9bb2-114">Пример 2. Создание определения политики с параметрами с параметрами</span><span class="sxs-lookup"><span data-stu-id="a9bb2-114">Example 2: Create a parameterized policy definition using inline parameters</span></span>
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

<span data-ttu-id="a9bb2-115">Эта команда создает определение политики LocationDefinition, которое содержит правило политики, указанное в C:\LocationPolicy.js.</span><span class="sxs-lookup"><span data-stu-id="a9bb2-115">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="a9bb2-116">Определение параметра для правила политики предоставляется в этом же окне.</span><span class="sxs-lookup"><span data-stu-id="a9bb2-116">The parameter definition for the policy rule is provided inline.</span></span>

### <span data-ttu-id="a9bb2-117">Пример 3. Создание определения политики в составе группы управления</span><span class="sxs-lookup"><span data-stu-id="a9bb2-117">Example 3: Create a policy definition inline in a management group</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName Dept42 -DisplayName 'Virtual Machine policy definition' -Policy '{"if":{"field":"type","equals":"Microsoft.Compute/virtualMachines"},"then":{"effect":"deny"}}'
```

<span data-ttu-id="a9bb2-118">Эта команда создает определение политики VMPolicyDefinition в группе управления Dept42.</span><span class="sxs-lookup"><span data-stu-id="a9bb2-118">This command creates a policy definition named VMPolicyDefinition in management group Dept42.</span></span>
<span data-ttu-id="a9bb2-119">Команда указывает политику как строку в допустимом формате JSON.</span><span class="sxs-lookup"><span data-stu-id="a9bb2-119">The command specifies the policy as a string in valid JSON format.</span></span>

### <span data-ttu-id="a9bb2-120">Пример 4. Создание определения политики с метаданными</span><span class="sxs-lookup"><span data-stu-id="a9bb2-120">Example 4: Create a policy definition inline with metadata</span></span>
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

<span data-ttu-id="a9bb2-121">Эта команда создает определение политики VMPolicyDefinition с метаданными, которые обозначают ее категорию "Виртуальная машинка".</span><span class="sxs-lookup"><span data-stu-id="a9bb2-121">This command creates a policy definition named VMPolicyDefinition with metadata indicating its category is "Virtual Machine".</span></span>
<span data-ttu-id="a9bb2-122">Команда указывает политику как строку в допустимом формате JSON.</span><span class="sxs-lookup"><span data-stu-id="a9bb2-122">The command specifies the policy as a string in valid JSON format.</span></span>

### <span data-ttu-id="a9bb2-123">Пример 5. Создание определения политики в режиме</span><span class="sxs-lookup"><span data-stu-id="a9bb2-123">Example 5: Create a policy definition inline with mode</span></span>
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

<span data-ttu-id="a9bb2-124">Эта команда создает определение политики TagsPolicyDefinition с режимом "Индексированное", указывающее, что политика должна оцениваться только для типов ресурсов, которые поддерживают теги и расположение.</span><span class="sxs-lookup"><span data-stu-id="a9bb2-124">This command creates a policy definition named TagsPolicyDefinition with mode "Indexed" indicating the policy should be evaluated only for resource types that support tags and location.</span></span>

## <span data-ttu-id="a9bb2-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9bb2-125">PARAMETERS</span></span>

### <span data-ttu-id="a9bb2-126">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a9bb2-126">-ApiVersion</span></span>
<span data-ttu-id="a9bb2-127">Определяет версию API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a9bb2-127">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="a9bb2-128">Если не указать версию, этот cmdlet использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="a9bb2-128">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="a9bb2-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9bb2-129">-DefaultProfile</span></span>
<span data-ttu-id="a9bb2-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a9bb2-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9bb2-131">-Description</span><span class="sxs-lookup"><span data-stu-id="a9bb2-131">-Description</span></span>
<span data-ttu-id="a9bb2-132">Описание определения политики.</span><span class="sxs-lookup"><span data-stu-id="a9bb2-132">Specifies a description for the policy definition.</span></span>

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

### <span data-ttu-id="a9bb2-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a9bb2-133">-DisplayName</span></span>
<span data-ttu-id="a9bb2-134">Указывает отображаемого имя определения политики.</span><span class="sxs-lookup"><span data-stu-id="a9bb2-134">Specifies a display name for the policy definition.</span></span>

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

### <span data-ttu-id="a9bb2-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="a9bb2-135">-ManagementGroupName</span></span>
<span data-ttu-id="a9bb2-136">Имя группы управления в новом определении политики.</span><span class="sxs-lookup"><span data-stu-id="a9bb2-136">The name of the management group of the new policy definition.</span></span>

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

### <span data-ttu-id="a9bb2-137">-Метаданные</span><span class="sxs-lookup"><span data-stu-id="a9bb2-137">-Metadata</span></span>
<span data-ttu-id="a9bb2-138">Метаданные определения политики.</span><span class="sxs-lookup"><span data-stu-id="a9bb2-138">The metadata for policy definition.</span></span> <span data-ttu-id="a9bb2-139">Это может быть путь к имени файла, содержащего метаданные, или метаданные в виде строки</span><span class="sxs-lookup"><span data-stu-id="a9bb2-139">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="a9bb2-140">-Mode</span><span class="sxs-lookup"><span data-stu-id="a9bb2-140">-Mode</span></span>
<span data-ttu-id="a9bb2-141">Режим определения политики</span><span class="sxs-lookup"><span data-stu-id="a9bb2-141">The mode of the policy definition</span></span>

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

### <span data-ttu-id="a9bb2-142">-Name</span><span class="sxs-lookup"><span data-stu-id="a9bb2-142">-Name</span></span>
<span data-ttu-id="a9bb2-143">Указывает имя определения политики.</span><span class="sxs-lookup"><span data-stu-id="a9bb2-143">Specifies a name for the policy definition.</span></span>

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

### <span data-ttu-id="a9bb2-144">-Parameter</span><span class="sxs-lookup"><span data-stu-id="a9bb2-144">-Parameter</span></span>
<span data-ttu-id="a9bb2-145">Объявление параметров для определения политики.</span><span class="sxs-lookup"><span data-stu-id="a9bb2-145">The parameters declaration for policy definition.</span></span> <span data-ttu-id="a9bb2-146">Это может быть путь к имени файла, содержащего объявление параметров, или объявление параметров в качестве строки.</span><span class="sxs-lookup"><span data-stu-id="a9bb2-146">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="a9bb2-147">-Политика</span><span class="sxs-lookup"><span data-stu-id="a9bb2-147">-Policy</span></span>
<span data-ttu-id="a9bb2-148">Определяет правило политики для определения политики.</span><span class="sxs-lookup"><span data-stu-id="a9bb2-148">Specifies a policy rule for the policy definition.</span></span>
<span data-ttu-id="a9bb2-149">Вы можете указать путь к JSON-файлу или строке, которая содержит политику в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="a9bb2-149">You can specify the path of a .json file or a string that contains the policy in JSON format.</span></span>

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

### <span data-ttu-id="a9bb2-150">-Pre</span><span class="sxs-lookup"><span data-stu-id="a9bb2-150">-Pre</span></span>
<span data-ttu-id="a9bb2-151">Указывает на то, что этот cmdlet рассматривает предварительные версии API при автоматическом определении используемой версии.</span><span class="sxs-lookup"><span data-stu-id="a9bb2-151">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a9bb2-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a9bb2-152">-SubscriptionId</span></span>
<span data-ttu-id="a9bb2-153">ИД подписки в новом определении политики.</span><span class="sxs-lookup"><span data-stu-id="a9bb2-153">The subscription ID of the new policy definition.</span></span>

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

### <span data-ttu-id="a9bb2-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9bb2-154">CommonParameters</span></span>
<span data-ttu-id="a9bb2-155">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9bb2-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9bb2-156">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9bb2-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9bb2-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a9bb2-157">INPUTS</span></span>

### <span data-ttu-id="a9bb2-158">System.String</span><span class="sxs-lookup"><span data-stu-id="a9bb2-158">System.String</span></span>

### <span data-ttu-id="a9bb2-159">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a9bb2-159">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a9bb2-160">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a9bb2-160">OUTPUTS</span></span>

### <span data-ttu-id="a9bb2-161">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="a9bb2-161">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a9bb2-162">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a9bb2-162">NOTES</span></span>

## <span data-ttu-id="a9bb2-163">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a9bb2-163">RELATED LINKS</span></span>

[<span data-ttu-id="a9bb2-164">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a9bb2-164">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="a9bb2-165">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a9bb2-165">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

[<span data-ttu-id="a9bb2-166">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a9bb2-166">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


