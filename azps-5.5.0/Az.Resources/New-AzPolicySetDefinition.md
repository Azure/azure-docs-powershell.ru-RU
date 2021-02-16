---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
ms.openlocfilehash: 1a4a2579b05c60133fa1b0f7ab057be602965eaa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226812"
---
# <span data-ttu-id="eb7a1-101">New-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="eb7a1-101">New-AzPolicySetDefinition</span></span>

## <span data-ttu-id="eb7a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb7a1-102">SYNOPSIS</span></span>
<span data-ttu-id="eb7a1-103">Создание определения набора политик.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-103">Creates a policy set definition.</span></span>

## <span data-ttu-id="eb7a1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="eb7a1-104">SYNTAX</span></span>

### <span data-ttu-id="eb7a1-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="eb7a1-105">NameParameterSet (Default)</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb7a1-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb7a1-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -ManagementGroupName <String> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eb7a1-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb7a1-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -SubscriptionId <Guid> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eb7a1-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb7a1-108">DESCRIPTION</span></span>
<span data-ttu-id="eb7a1-109">Для **создания определения набора политик создается cmdlet New-AzPolicySetDefinition.**</span><span class="sxs-lookup"><span data-stu-id="eb7a1-109">The **New-AzPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="eb7a1-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="eb7a1-110">EXAMPLES</span></span>

### <span data-ttu-id="eb7a1-111">Пример 1. Создание определения набора политики с метаданными с помощью файла набора политики</span><span class="sxs-lookup"><span data-stu-id="eb7a1-111">Example 1: Create a policy set definition with metadata by using a policy set file</span></span>
```
[
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/2a0e14a6-b0a6-4fab-991a-187a4f81c498",
      "parameters": {
         "tagName": {
            "value": "Business Unit"
         },
         "tagValue": {
            "value": "Finance"
         }
      }
   },
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/464dbb85-3d5f-4a1d-bb09-95a9b5dd19cf"
   }
]
```

```
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -Metadata '{"category":"Virtual Machine"}' -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="eb7a1-112">Эта команда создает определение набора политики vMPolicySetDefinition с метаданными, которые обозначают категорию "Виртуальная машинка", которая содержит определения политики, указанные в C:\VMPolicy.js.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-112">This command creates a policy set definition named VMPolicySetDefinition with metadata indicating its category is "Virtual Machine" that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="eb7a1-113">Пример содержимого VMPolicy.jsвыше.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-113">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="eb7a1-114">Пример 2. Создание определения набора политики с параметрами</span><span class="sxs-lookup"><span data-stu-id="eb7a1-114">Example 2: Create a parameterized policy set definition</span></span>
```
[
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/2a0e14a6-b0a6-4fab-991a-187a4f81c498",
      "parameters": {
         "tagName": {
            "value": "Business Unit"
         },
         "tagValue": {
            "value": "[parameters('buTagValue')]"
         }
      }
   },
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/464dbb85-3d5f-4a1d-bb09-95a9b5dd19cf"
   }
]
```

```
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -PolicyDefinition C:\VMPolicySet.json -Parameter '{ "buTagValue": { "type": "string" } }'
```

<span data-ttu-id="eb7a1-115">Эта команда создает определение набора с параметрами под названием VMPolicySetDefinition, которое содержит определения политики, заданные C:\VMPolicy.jsполитиках.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-115">This command creates a parameterized policy set definition named VMPolicySetDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="eb7a1-116">Пример содержимого VMPolicy.jsвыше.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-116">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="eb7a1-117">Пример 3. Создание определения набора политик с помощью групп определений политик</span><span class="sxs-lookup"><span data-stu-id="eb7a1-117">Example 3: Create a policy set definition with policy definition groups</span></span>
```
[
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/2a0e14a6-b0a6-4fab-991a-187a4f81c498",
      "groupNames": [ "group1" ]
   },
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/464dbb85-3d5f-4a1d-bb09-95a9b5dd19cf",
      "groupNames": [ "group2" ]
   }
]
```

```
$groupsJson = ConvertTo-Json @{ name = "group1" }, @{ name = "group2" }
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition $groupsJson -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="eb7a1-118">Эта команда создает определение набора политики VMPolicySetDefinition с группировкой определений политики, заданной в C:\VMPolicy.jsполитиках.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-118">This command creates a policy set definition named VMPolicySetDefinition with grouping of policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="eb7a1-119">Пример содержимого VMPolicy.jsвыше.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-119">Example content of the VMPolicy.json is provided above.</span></span>

## <span data-ttu-id="eb7a1-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb7a1-120">PARAMETERS</span></span>

### <span data-ttu-id="eb7a1-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="eb7a1-121">-ApiVersion</span></span>
<span data-ttu-id="eb7a1-122">Указывает на версию API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-122">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="eb7a1-123">Если он не задан, версия API будет автоматически определена как наиболее последняя из доступных.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-123">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="eb7a1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb7a1-124">-DefaultProfile</span></span>
<span data-ttu-id="eb7a1-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="eb7a1-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb7a1-126">-Description</span><span class="sxs-lookup"><span data-stu-id="eb7a1-126">-Description</span></span>
<span data-ttu-id="eb7a1-127">Описание определения набора политик.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-127">The description for policy set definition.</span></span>

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

### <span data-ttu-id="eb7a1-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="eb7a1-128">-DisplayName</span></span>
<span data-ttu-id="eb7a1-129">Отображаемого имени определения набора политик.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-129">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="eb7a1-130">-GroupDefinition</span><span class="sxs-lookup"><span data-stu-id="eb7a1-130">-GroupDefinition</span></span>
<span data-ttu-id="eb7a1-131">Группы определений политик для определения нового набора политик.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-131">The policy definition groups for the new policy set definition.</span></span> <span data-ttu-id="eb7a1-132">Это может быть путь к файлу, содержащего группы, или группы в качестве строки JSON.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-132">This can either be a path to a file containing the groups, or the groups as a JSON string.</span></span>

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

### <span data-ttu-id="eb7a1-133">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="eb7a1-133">-ManagementGroupName</span></span>
<span data-ttu-id="eb7a1-134">Имя группы управления определения нового набора политик.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-134">The name of the management group of the new policy set definition.</span></span>

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

### <span data-ttu-id="eb7a1-135">-Метаданные</span><span class="sxs-lookup"><span data-stu-id="eb7a1-135">-Metadata</span></span>
<span data-ttu-id="eb7a1-136">Метаданные для определения набора политики.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-136">The metadata for policy set definition.</span></span> <span data-ttu-id="eb7a1-137">Это может быть путь к имени файла, содержащего метаданные, или метаданные в виде строки JSON.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-137">This can either be a path to a file name containing the metadata, or the metadata as a JSON string.</span></span>

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

### <span data-ttu-id="eb7a1-138">-Name</span><span class="sxs-lookup"><span data-stu-id="eb7a1-138">-Name</span></span>
<span data-ttu-id="eb7a1-139">Имя определения набора политики.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-139">The policy set definition name.</span></span>

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

### <span data-ttu-id="eb7a1-140">-Parameter</span><span class="sxs-lookup"><span data-stu-id="eb7a1-140">-Parameter</span></span>
<span data-ttu-id="eb7a1-141">Объявление параметров для определения набора политик.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-141">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="eb7a1-142">Это может быть путь к имени файла, содержащего объявление параметров, или объявление параметров в качестве строки JSON.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-142">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as a JSON string.</span></span>

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

### <span data-ttu-id="eb7a1-143">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="eb7a1-143">-PolicyDefinition</span></span>
<span data-ttu-id="eb7a1-144">Определения политик.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-144">The policy definitions.</span></span> <span data-ttu-id="eb7a1-145">Это может быть путь к имени файла, содержащего определения политики, или определения политики в качестве строки JSON.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-145">This can either be a path to a file name containing the policy definitions, or the policy definitions as a JSON string.</span></span>

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

### <span data-ttu-id="eb7a1-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="eb7a1-146">-Pre</span></span>
<span data-ttu-id="eb7a1-147">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-147">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="eb7a1-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eb7a1-148">-SubscriptionId</span></span>
<span data-ttu-id="eb7a1-149">The subscription ID of the new policy set definition.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-149">The subscription ID of the new policy set definition.</span></span>

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

### <span data-ttu-id="eb7a1-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eb7a1-150">-Confirm</span></span>
<span data-ttu-id="eb7a1-151">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb7a1-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb7a1-152">-WhatIf</span></span>
<span data-ttu-id="eb7a1-153">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eb7a1-154">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-154">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb7a1-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb7a1-155">CommonParameters</span></span>
<span data-ttu-id="eb7a1-156">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb7a1-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb7a1-157">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eb7a1-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb7a1-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eb7a1-158">INPUTS</span></span>

### <span data-ttu-id="eb7a1-159">System.String</span><span class="sxs-lookup"><span data-stu-id="eb7a1-159">System.String</span></span>

### <span data-ttu-id="eb7a1-160">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="eb7a1-160">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="eb7a1-161">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="eb7a1-161">OUTPUTS</span></span>

### <span data-ttu-id="eb7a1-162">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="eb7a1-162">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="eb7a1-163">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="eb7a1-163">NOTES</span></span>

## <span data-ttu-id="eb7a1-164">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eb7a1-164">RELATED LINKS</span></span>
