---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
ms.openlocfilehash: 1a4a2579b05c60133fa1b0f7ab057be602965eaa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235892"
---
# <span data-ttu-id="4cc11-101">New-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="4cc11-101">New-AzPolicySetDefinition</span></span>

## <span data-ttu-id="4cc11-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4cc11-102">SYNOPSIS</span></span>
<span data-ttu-id="4cc11-103">Создание определения множества политик.</span><span class="sxs-lookup"><span data-stu-id="4cc11-103">Creates a policy set definition.</span></span>

## <span data-ttu-id="4cc11-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4cc11-104">SYNTAX</span></span>

### <span data-ttu-id="4cc11-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4cc11-105">NameParameterSet (Default)</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cc11-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4cc11-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -ManagementGroupName <String> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4cc11-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4cc11-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -SubscriptionId <Guid> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4cc11-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4cc11-108">DESCRIPTION</span></span>
<span data-ttu-id="4cc11-109">Командлет **New-AzPolicySetDefinition** создает определение политики.</span><span class="sxs-lookup"><span data-stu-id="4cc11-109">The **New-AzPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="4cc11-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4cc11-110">EXAMPLES</span></span>

### <span data-ttu-id="4cc11-111">Пример 1: Создание определения политики с метаданными с помощью файла Set политики</span><span class="sxs-lookup"><span data-stu-id="4cc11-111">Example 1: Create a policy set definition with metadata by using a policy set file</span></span>
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

<span data-ttu-id="4cc11-112">Эта команда создает определение политики с именем VMPolicySetDefinition с метаданными, указывающими на ее категорию "виртуальная машина", которая содержит определения политик, указанные в C:\VMPolicy.json.</span><span class="sxs-lookup"><span data-stu-id="4cc11-112">This command creates a policy set definition named VMPolicySetDefinition with metadata indicating its category is "Virtual Machine" that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="4cc11-113">Ниже приведен пример содержимого VMPolicy.json.</span><span class="sxs-lookup"><span data-stu-id="4cc11-113">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="4cc11-114">Пример 2: Создание определения параметризованной политики</span><span class="sxs-lookup"><span data-stu-id="4cc11-114">Example 2: Create a parameterized policy set definition</span></span>
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

<span data-ttu-id="4cc11-115">Эта команда создает параметризованный набор политик с именем VMPolicySetDefinition, который включает в себя определения политик, указанные в C:\VMPolicy.json.</span><span class="sxs-lookup"><span data-stu-id="4cc11-115">This command creates a parameterized policy set definition named VMPolicySetDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="4cc11-116">Ниже приведен пример содержимого VMPolicy.json.</span><span class="sxs-lookup"><span data-stu-id="4cc11-116">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="4cc11-117">Пример 3: Создание определения политики с помощью групп определения политики</span><span class="sxs-lookup"><span data-stu-id="4cc11-117">Example 3: Create a policy set definition with policy definition groups</span></span>
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

<span data-ttu-id="4cc11-118">Эта команда создает определение политики с именем VMPolicySetDefinition и задает группировку определений политик, указанных в C:\VMPolicy.json.</span><span class="sxs-lookup"><span data-stu-id="4cc11-118">This command creates a policy set definition named VMPolicySetDefinition with grouping of policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="4cc11-119">Ниже приведен пример содержимого VMPolicy.json.</span><span class="sxs-lookup"><span data-stu-id="4cc11-119">Example content of the VMPolicy.json is provided above.</span></span>

## <span data-ttu-id="4cc11-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4cc11-120">PARAMETERS</span></span>

### <span data-ttu-id="4cc11-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4cc11-121">-ApiVersion</span></span>
<span data-ttu-id="4cc11-122">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4cc11-122">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="4cc11-123">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="4cc11-123">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="4cc11-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cc11-124">-DefaultProfile</span></span>
<span data-ttu-id="4cc11-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4cc11-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4cc11-126">-Описание</span><span class="sxs-lookup"><span data-stu-id="4cc11-126">-Description</span></span>
<span data-ttu-id="4cc11-127">Описание определения политики.</span><span class="sxs-lookup"><span data-stu-id="4cc11-127">The description for policy set definition.</span></span>

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

### <span data-ttu-id="4cc11-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4cc11-128">-DisplayName</span></span>
<span data-ttu-id="4cc11-129">Отображаемое имя определения множества политик.</span><span class="sxs-lookup"><span data-stu-id="4cc11-129">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="4cc11-130">-GroupDefinition</span><span class="sxs-lookup"><span data-stu-id="4cc11-130">-GroupDefinition</span></span>
<span data-ttu-id="4cc11-131">Группы определений политики для нового определения множества политик.</span><span class="sxs-lookup"><span data-stu-id="4cc11-131">The policy definition groups for the new policy set definition.</span></span> <span data-ttu-id="4cc11-132">Это может быть либо путь к файлу, содержащему группы, либо группам в виде строки JSON.</span><span class="sxs-lookup"><span data-stu-id="4cc11-132">This can either be a path to a file containing the groups, or the groups as a JSON string.</span></span>

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

### <span data-ttu-id="4cc11-133">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="4cc11-133">-ManagementGroupName</span></span>
<span data-ttu-id="4cc11-134">Имя группы управления для нового определения набора политик.</span><span class="sxs-lookup"><span data-stu-id="4cc11-134">The name of the management group of the new policy set definition.</span></span>

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

### <span data-ttu-id="4cc11-135">-Metadata</span><span class="sxs-lookup"><span data-stu-id="4cc11-135">-Metadata</span></span>
<span data-ttu-id="4cc11-136">Метаданные для определения Set политики.</span><span class="sxs-lookup"><span data-stu-id="4cc11-136">The metadata for policy set definition.</span></span> <span data-ttu-id="4cc11-137">Это может быть либо путь к имени файла, содержащему метаданные, либо метаданные в виде строки JSON.</span><span class="sxs-lookup"><span data-stu-id="4cc11-137">This can either be a path to a file name containing the metadata, or the metadata as a JSON string.</span></span>

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

### <span data-ttu-id="4cc11-138">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4cc11-138">-Name</span></span>
<span data-ttu-id="4cc11-139">Имя определения настройки политики.</span><span class="sxs-lookup"><span data-stu-id="4cc11-139">The policy set definition name.</span></span>

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

### <span data-ttu-id="4cc11-140">-Параметр</span><span class="sxs-lookup"><span data-stu-id="4cc11-140">-Parameter</span></span>
<span data-ttu-id="4cc11-141">Объявление параметров для определения задания политики.</span><span class="sxs-lookup"><span data-stu-id="4cc11-141">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="4cc11-142">Это может быть путь к имени файла, содержащему объявление параметров, или объявление параметров в виде строки JSON.</span><span class="sxs-lookup"><span data-stu-id="4cc11-142">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as a JSON string.</span></span>

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

### <span data-ttu-id="4cc11-143">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4cc11-143">-PolicyDefinition</span></span>
<span data-ttu-id="4cc11-144">Определения политики.</span><span class="sxs-lookup"><span data-stu-id="4cc11-144">The policy definitions.</span></span> <span data-ttu-id="4cc11-145">Это может быть путь к имени файла, содержащему определения политики, или определениям политики в виде строки JSON.</span><span class="sxs-lookup"><span data-stu-id="4cc11-145">This can either be a path to a file name containing the policy definitions, or the policy definitions as a JSON string.</span></span>

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

### <span data-ttu-id="4cc11-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="4cc11-146">-Pre</span></span>
<span data-ttu-id="4cc11-147">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="4cc11-147">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="4cc11-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4cc11-148">-SubscriptionId</span></span>
<span data-ttu-id="4cc11-149">Идентификатор подписки нового определения набора политики.</span><span class="sxs-lookup"><span data-stu-id="4cc11-149">The subscription ID of the new policy set definition.</span></span>

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

### <span data-ttu-id="4cc11-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4cc11-150">-Confirm</span></span>
<span data-ttu-id="4cc11-151">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4cc11-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cc11-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cc11-152">-WhatIf</span></span>
<span data-ttu-id="4cc11-153">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4cc11-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4cc11-154">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4cc11-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cc11-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cc11-155">CommonParameters</span></span>
<span data-ttu-id="4cc11-156">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4cc11-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cc11-157">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4cc11-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cc11-158">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4cc11-158">INPUTS</span></span>

### <span data-ttu-id="4cc11-159">System. String</span><span class="sxs-lookup"><span data-stu-id="4cc11-159">System.String</span></span>

### <span data-ttu-id="4cc11-160">System. Nullable "1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4cc11-160">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="4cc11-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4cc11-161">OUTPUTS</span></span>

### <span data-ttu-id="4cc11-162">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="4cc11-162">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="4cc11-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="4cc11-163">NOTES</span></span>

## <span data-ttu-id="4cc11-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4cc11-164">RELATED LINKS</span></span>
