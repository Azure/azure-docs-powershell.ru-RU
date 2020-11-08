---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
ms.openlocfilehash: cd8bc24a0cedac91ef18e19a80e1662fdcbac297
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235877"
---
# <span data-ttu-id="044b3-101">Set-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="044b3-101">Set-AzPolicySetDefinition</span></span>

## <span data-ttu-id="044b3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="044b3-102">SYNOPSIS</span></span>
<span data-ttu-id="044b3-103">Изменение определения Set политики</span><span class="sxs-lookup"><span data-stu-id="044b3-103">Modifies a policy set definition</span></span>

## <span data-ttu-id="044b3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="044b3-104">SYNTAX</span></span>

### <span data-ttu-id="044b3-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="044b3-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="044b3-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="044b3-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -ManagementGroupName <String>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="044b3-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="044b3-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -SubscriptionId <Guid>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="044b3-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="044b3-108">IdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="044b3-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="044b3-109">InputObjectParameterSet</span></span>
```
Set-AzPolicySetDefinition [-DisplayName <String>] [-Description <String>] [-PolicyDefinition <String>]
 [-Metadata <String>] [-Parameter <String>] -InputObject <PsPolicySetDefinition> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="044b3-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="044b3-110">DESCRIPTION</span></span>
<span data-ttu-id="044b3-111">Командлет **Set-AzPolicySetDefinition** изменяет определение политики.</span><span class="sxs-lookup"><span data-stu-id="044b3-111">The **Set-AzPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="044b3-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="044b3-112">EXAMPLES</span></span>

### <span data-ttu-id="044b3-113">Пример 1: Обновление описания определения набора политик</span><span class="sxs-lookup"><span data-stu-id="044b3-113">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Set-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="044b3-114">Первая команда получает определение политики с помощью командлета Get-AzPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="044b3-114">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="044b3-115">Команда сохраняет этот объект в переменной $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="044b3-115">The command stores that object in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="044b3-116">Вторая команда обновляет описание определения политики, определяемое свойством **ResourceId** для $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="044b3-116">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

### <span data-ttu-id="044b3-117">Пример 2: обновление метаданных определения набора политик</span><span class="sxs-lookup"><span data-stu-id="044b3-117">Example 2: Update the metadata of a policy set definition</span></span>
```
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -Metadata '{"category":"Virtual Machine"}'


Name                  : VMPolicySetDefinition
ResourceId            : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policySetDefinitions/VMPolicySetDefinition
ResourceName          : VMPolicySetDefinition
ResourceType          : Microsoft.Authorization/policySetDefinitions
SubscriptionId        : 11111111-1111-1111-1111-111111111111
Properties            : @{displayName=VMPolicySetDefinition; policyType=Custom; metadata=; parameters=; policyDefinitions=System.Object[]}
PolicySetDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policySetDefinitions/VMPolicySetDefinition
```

<span data-ttu-id="044b3-118">Эта команда обновляет метаданные определения Set политики с именем VMPolicySetDefinition, чтобы указать, что ее Категория — "виртуальная машина".</span><span class="sxs-lookup"><span data-stu-id="044b3-118">This command updates the metadata of a policy set definition named VMPolicySetDefinition to indicate its category is "Virtual Machine".</span></span>

### <span data-ttu-id="044b3-119">Пример 3: обновление групп определения набора политик</span><span class="sxs-lookup"><span data-stu-id="044b3-119">Example 3: Update the groups of a policy set definition</span></span>
```
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition '[{ "name": "group1", "displayName": "Virtual Machine Security" }, { "name": "group2" }]'
```

<span data-ttu-id="044b3-120">Эта команда обновляет группы определения набора политик с именем VMPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="044b3-120">This command updates the groups of a policy set definition named VMPolicySetDefinition.</span></span>

### <span data-ttu-id="044b3-121">Пример 4: обновление групп определения политики с помощью хэш-таблицы</span><span class="sxs-lookup"><span data-stu-id="044b3-121">Example 4: Update the groups of a policy set definition using a hash table</span></span>
```
$groupsJson = ConvertTo-Json @{ name = "group1", displayName = "Virtual Machine Security" }, @{ name = "group2" }
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition $groupsJson
```

<span data-ttu-id="044b3-122">Эта команда обновляет группы с определением набора политик с именем VMPolicySetDefinition, используя хэш-таблицу для создания групп.</span><span class="sxs-lookup"><span data-stu-id="044b3-122">This command updates the groups of a policy set definition named VMPolicySetDefinition using a hash table to construct the groups.</span></span>

## <span data-ttu-id="044b3-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="044b3-123">PARAMETERS</span></span>

### <span data-ttu-id="044b3-124">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="044b3-124">-ApiVersion</span></span>
<span data-ttu-id="044b3-125">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="044b3-125">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="044b3-126">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="044b3-126">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="044b3-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="044b3-127">-DefaultProfile</span></span>
<span data-ttu-id="044b3-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="044b3-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="044b3-129">-Описание</span><span class="sxs-lookup"><span data-stu-id="044b3-129">-Description</span></span>
<span data-ttu-id="044b3-130">Описание определения политики.</span><span class="sxs-lookup"><span data-stu-id="044b3-130">The description for policy set definition.</span></span>

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

### <span data-ttu-id="044b3-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="044b3-131">-DisplayName</span></span>
<span data-ttu-id="044b3-132">Отображаемое имя определения множества политик.</span><span class="sxs-lookup"><span data-stu-id="044b3-132">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="044b3-133">-GroupDefinition</span><span class="sxs-lookup"><span data-stu-id="044b3-133">-GroupDefinition</span></span>
<span data-ttu-id="044b3-134">Группы определений политики для обновленного определения набора политик.</span><span class="sxs-lookup"><span data-stu-id="044b3-134">The policy definition groups of the updated policy set definition.</span></span> <span data-ttu-id="044b3-135">Это может быть либо путь к файлу, содержащему группы, либо группам в виде строки JSON.</span><span class="sxs-lookup"><span data-stu-id="044b3-135">This can either be a path to a file containing the groups, or the groups as a JSON string.</span></span>

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

### <span data-ttu-id="044b3-136">-ID</span><span class="sxs-lookup"><span data-stu-id="044b3-136">-Id</span></span>
<span data-ttu-id="044b3-137">Полный идентификатор определения политики, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="044b3-137">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="044b3-138">Например,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="044b3-138">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="044b3-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="044b3-139">-InputObject</span></span>
<span data-ttu-id="044b3-140">Объект определения политики для обновления, полученный в результате выхода другого командлета.</span><span class="sxs-lookup"><span data-stu-id="044b3-140">The policy set definition object to update that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicySetDefinition
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="044b3-141">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="044b3-141">-ManagementGroupName</span></span>
<span data-ttu-id="044b3-142">Имя группы управления для определения политики, которую требуется обновить.</span><span class="sxs-lookup"><span data-stu-id="044b3-142">The name of the management group of the policy set definition to update.</span></span>

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

### <span data-ttu-id="044b3-143">-Metadata</span><span class="sxs-lookup"><span data-stu-id="044b3-143">-Metadata</span></span>
<span data-ttu-id="044b3-144">Метаданные определения обновленного набора политик.</span><span class="sxs-lookup"><span data-stu-id="044b3-144">The metadata of the updated policy set definition.</span></span> <span data-ttu-id="044b3-145">Это может быть либо путь к имени файла, содержащему метаданные, либо метаданные в виде строки JSON.</span><span class="sxs-lookup"><span data-stu-id="044b3-145">This can either be a path to a file name containing the metadata, or the metadata as a JSON string.</span></span>

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

### <span data-ttu-id="044b3-146">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="044b3-146">-Name</span></span>
<span data-ttu-id="044b3-147">Имя определения настройки политики.</span><span class="sxs-lookup"><span data-stu-id="044b3-147">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="044b3-148">-Параметр</span><span class="sxs-lookup"><span data-stu-id="044b3-148">-Parameter</span></span>
<span data-ttu-id="044b3-149">Объявление параметров обновленного определения набора политик.</span><span class="sxs-lookup"><span data-stu-id="044b3-149">The parameters declaration of the updated policy set definition.</span></span> <span data-ttu-id="044b3-150">Это может быть путь к имени файла или универсальному коду ресурса (URI), содержащему объявление параметров, или объявление параметров в виде строки JSON.</span><span class="sxs-lookup"><span data-stu-id="044b3-150">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as a JSON string.</span></span>

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

### <span data-ttu-id="044b3-151">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="044b3-151">-PolicyDefinition</span></span>
<span data-ttu-id="044b3-152">Определения политики.</span><span class="sxs-lookup"><span data-stu-id="044b3-152">The policy definitions.</span></span> <span data-ttu-id="044b3-153">Это может быть путь к имени файла, содержащему определения политики, или определениям политики в виде строки JSON.</span><span class="sxs-lookup"><span data-stu-id="044b3-153">This can either be a path to a file name containing the policy definitions, or the policy definitions as a JSON string.</span></span>

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

### <span data-ttu-id="044b3-154">-Pre</span><span class="sxs-lookup"><span data-stu-id="044b3-154">-Pre</span></span>
<span data-ttu-id="044b3-155">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="044b3-155">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="044b3-156">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="044b3-156">-SubscriptionId</span></span>
<span data-ttu-id="044b3-157">Идентификатор подписки для определения политики, которую требуется обновить.</span><span class="sxs-lookup"><span data-stu-id="044b3-157">The subscription ID of the policy set definition to update.</span></span>

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

### <span data-ttu-id="044b3-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="044b3-158">-Confirm</span></span>
<span data-ttu-id="044b3-159">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="044b3-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="044b3-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="044b3-160">-WhatIf</span></span>
<span data-ttu-id="044b3-161">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="044b3-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="044b3-162">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="044b3-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="044b3-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="044b3-163">CommonParameters</span></span>
<span data-ttu-id="044b3-164">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="044b3-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="044b3-165">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="044b3-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="044b3-166">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="044b3-166">INPUTS</span></span>

### <span data-ttu-id="044b3-167">System. String</span><span class="sxs-lookup"><span data-stu-id="044b3-167">System.String</span></span>

### <span data-ttu-id="044b3-168">System. Nullable "1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="044b3-168">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="044b3-169">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="044b3-169">OUTPUTS</span></span>

### <span data-ttu-id="044b3-170">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="044b3-170">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="044b3-171">Пуск</span><span class="sxs-lookup"><span data-stu-id="044b3-171">NOTES</span></span>

## <span data-ttu-id="044b3-172">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="044b3-172">RELATED LINKS</span></span>
