---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
ms.openlocfilehash: cf1f1993c58e9c87c36538199555e5ebd7c2175a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729381"
---
# <span data-ttu-id="022b0-101">New-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="022b0-101">New-AzPolicySetDefinition</span></span>

## <span data-ttu-id="022b0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="022b0-102">SYNOPSIS</span></span>
<span data-ttu-id="022b0-103">Создание определения множества политик.</span><span class="sxs-lookup"><span data-stu-id="022b0-103">Creates a policy set definition.</span></span>

## <span data-ttu-id="022b0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="022b0-104">SYNTAX</span></span>

### <span data-ttu-id="022b0-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="022b0-105">NameParameterSet (Default)</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="022b0-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="022b0-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="022b0-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="022b0-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="022b0-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="022b0-108">DESCRIPTION</span></span>
<span data-ttu-id="022b0-109">Командлет **New-AzPolicySetDefinition** создает определение политики.</span><span class="sxs-lookup"><span data-stu-id="022b0-109">The **New-AzPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="022b0-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="022b0-110">EXAMPLES</span></span>

### <span data-ttu-id="022b0-111">Пример 1: Создание определения политики с помощью файла Set политики</span><span class="sxs-lookup"><span data-stu-id="022b0-111">Example 1: Create a policy set definition by using a policy set file</span></span>
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
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicyDefinition' -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="022b0-112">Эта команда создает определение политики с именем VMPolicyDefinition, которое включает определения политик, указанные в C:\VMPolicy.json.</span><span class="sxs-lookup"><span data-stu-id="022b0-112">This command creates a policy set definition named VMPolicyDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="022b0-113">Ниже приведен пример содержимого VMPolicy.json.</span><span class="sxs-lookup"><span data-stu-id="022b0-113">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="022b0-114">Пример 2: Создание определения параметризованной политики</span><span class="sxs-lookup"><span data-stu-id="022b0-114">Example 2: Create a parameterized policy set definition</span></span>
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
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicyDefinition' -PolicyDefinition C:\VMPolicySet.json -Parameter '{ "buTagValue": { "type": "string" } }'
```

<span data-ttu-id="022b0-115">Эта команда создает параметризованный набор политик с именем VMPolicyDefinition, который включает в себя определения политик, указанные в C:\VMPolicy.json.</span><span class="sxs-lookup"><span data-stu-id="022b0-115">This command creates a parameterized policy set definition named VMPolicyDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="022b0-116">Ниже приведен пример содержимого VMPolicy.json.</span><span class="sxs-lookup"><span data-stu-id="022b0-116">Example content of the VMPolicy.json is provided above.</span></span>

## <span data-ttu-id="022b0-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="022b0-117">PARAMETERS</span></span>

### <span data-ttu-id="022b0-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="022b0-118">-ApiVersion</span></span>
<span data-ttu-id="022b0-119">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="022b0-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="022b0-120">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="022b0-120">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="022b0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="022b0-121">-DefaultProfile</span></span>
<span data-ttu-id="022b0-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="022b0-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="022b0-123">-Описание</span><span class="sxs-lookup"><span data-stu-id="022b0-123">-Description</span></span>
<span data-ttu-id="022b0-124">Описание определения политики.</span><span class="sxs-lookup"><span data-stu-id="022b0-124">The description for policy set definition.</span></span>

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

### <span data-ttu-id="022b0-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="022b0-125">-DisplayName</span></span>
<span data-ttu-id="022b0-126">Отображаемое имя определения множества политик.</span><span class="sxs-lookup"><span data-stu-id="022b0-126">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="022b0-127">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="022b0-127">-ManagementGroupName</span></span>
<span data-ttu-id="022b0-128">Имя группы управления для нового определения набора политик.</span><span class="sxs-lookup"><span data-stu-id="022b0-128">The name of the management group of the new policy set definition.</span></span>

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

### <span data-ttu-id="022b0-129">-Metadata</span><span class="sxs-lookup"><span data-stu-id="022b0-129">-Metadata</span></span>
<span data-ttu-id="022b0-130">Метаданные для определения Set политики.</span><span class="sxs-lookup"><span data-stu-id="022b0-130">The metadata for policy set definition.</span></span> <span data-ttu-id="022b0-131">Это может быть путь к имени файла, содержащему метаданные, или метаданным в виде строки.</span><span class="sxs-lookup"><span data-stu-id="022b0-131">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="022b0-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="022b0-132">-Name</span></span>
<span data-ttu-id="022b0-133">Имя определения настройки политики.</span><span class="sxs-lookup"><span data-stu-id="022b0-133">The policy set definition name.</span></span>

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

### <span data-ttu-id="022b0-134">-Параметр</span><span class="sxs-lookup"><span data-stu-id="022b0-134">-Parameter</span></span>
<span data-ttu-id="022b0-135">Объявление параметров для определения задания политики.</span><span class="sxs-lookup"><span data-stu-id="022b0-135">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="022b0-136">Это может быть путь к имени файла, в котором содержится объявление параметров, или объявление параметров как String.</span><span class="sxs-lookup"><span data-stu-id="022b0-136">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="022b0-137">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="022b0-137">-PolicyDefinition</span></span>
<span data-ttu-id="022b0-138">Определение настройки политики.</span><span class="sxs-lookup"><span data-stu-id="022b0-138">The policy set definition.</span></span> <span data-ttu-id="022b0-139">Это может быть путь к имени файла, содержащему определения политики, или определению политики как String.</span><span class="sxs-lookup"><span data-stu-id="022b0-139">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

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

### <span data-ttu-id="022b0-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="022b0-140">-Pre</span></span>
<span data-ttu-id="022b0-141">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="022b0-141">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="022b0-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="022b0-142">-SubscriptionId</span></span>
<span data-ttu-id="022b0-143">Идентификатор подписки нового определения набора политики.</span><span class="sxs-lookup"><span data-stu-id="022b0-143">The subscription ID of the new policy set definition.</span></span>

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

### <span data-ttu-id="022b0-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="022b0-144">-Confirm</span></span>
<span data-ttu-id="022b0-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="022b0-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="022b0-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="022b0-146">-WhatIf</span></span>
<span data-ttu-id="022b0-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="022b0-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="022b0-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="022b0-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="022b0-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="022b0-149">CommonParameters</span></span>
<span data-ttu-id="022b0-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="022b0-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="022b0-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="022b0-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="022b0-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="022b0-152">INPUTS</span></span>

### <span data-ttu-id="022b0-153">System. String</span><span class="sxs-lookup"><span data-stu-id="022b0-153">System.String</span></span>

### <span data-ttu-id="022b0-154">System. Nullable "1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="022b0-154">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="022b0-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="022b0-155">OUTPUTS</span></span>

### <span data-ttu-id="022b0-156">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="022b0-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="022b0-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="022b0-157">NOTES</span></span>

## <span data-ttu-id="022b0-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="022b0-158">RELATED LINKS</span></span>
