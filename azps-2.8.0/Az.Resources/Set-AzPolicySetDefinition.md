---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
ms.openlocfilehash: 5b6d514fc41c909fdd48b6a13ba85ab5836a5668
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905501"
---
# <span data-ttu-id="c8d84-101">Set-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="c8d84-101">Set-AzPolicySetDefinition</span></span>

## <span data-ttu-id="c8d84-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c8d84-102">SYNOPSIS</span></span>
<span data-ttu-id="c8d84-103">Изменение определения Set политики</span><span class="sxs-lookup"><span data-stu-id="c8d84-103">Modifies a policy set definition</span></span>

## <span data-ttu-id="c8d84-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c8d84-104">SYNTAX</span></span>

### <span data-ttu-id="c8d84-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c8d84-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8d84-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8d84-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c8d84-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8d84-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c8d84-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8d84-108">IdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8d84-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8d84-109">DESCRIPTION</span></span>
<span data-ttu-id="c8d84-110">Командлет **Set-AzPolicySetDefinition** изменяет определение политики.</span><span class="sxs-lookup"><span data-stu-id="c8d84-110">The **Set-AzPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="c8d84-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c8d84-111">EXAMPLES</span></span>

### <span data-ttu-id="c8d84-112">Пример 1: Обновление описания определения набора политик</span><span class="sxs-lookup"><span data-stu-id="c8d84-112">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Set-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="c8d84-113">Первая команда получает определение политики с помощью командлета Get-AzPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="c8d84-113">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="c8d84-114">Команда сохраняет этот объект в переменной $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="c8d84-114">The command stores that object in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="c8d84-115">Вторая команда обновляет описание определения политики, определяемое свойством **ResourceId** для $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="c8d84-115">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

### <span data-ttu-id="c8d84-116">Пример 2: обновление метаданных определения набора политик</span><span class="sxs-lookup"><span data-stu-id="c8d84-116">Example 2: Update the metadata of a policy set definition</span></span>
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

<span data-ttu-id="c8d84-117">Эта команда обновляет метаданные определения Set политики с именем VMPolicySetDefinition, чтобы указать, что ее Категория — "виртуальная машина".</span><span class="sxs-lookup"><span data-stu-id="c8d84-117">This command updates the metadata of a policy set definition named VMPolicySetDefinition to indicate its category is "Virtual Machine".</span></span>

## <span data-ttu-id="c8d84-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c8d84-118">PARAMETERS</span></span>

### <span data-ttu-id="c8d84-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c8d84-119">-ApiVersion</span></span>
<span data-ttu-id="c8d84-120">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c8d84-120">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="c8d84-121">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="c8d84-121">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="c8d84-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8d84-122">-DefaultProfile</span></span>
<span data-ttu-id="c8d84-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c8d84-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8d84-124">-Описание</span><span class="sxs-lookup"><span data-stu-id="c8d84-124">-Description</span></span>
<span data-ttu-id="c8d84-125">Описание определения политики.</span><span class="sxs-lookup"><span data-stu-id="c8d84-125">The description for policy set definition.</span></span>

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

### <span data-ttu-id="c8d84-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c8d84-126">-DisplayName</span></span>
<span data-ttu-id="c8d84-127">Отображаемое имя определения множества политик.</span><span class="sxs-lookup"><span data-stu-id="c8d84-127">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="c8d84-128">-ID</span><span class="sxs-lookup"><span data-stu-id="c8d84-128">-Id</span></span>
<span data-ttu-id="c8d84-129">Полный идентификатор определения политики, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="c8d84-129">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="c8d84-130">Например,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="c8d84-130">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="c8d84-131">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="c8d84-131">-ManagementGroupName</span></span>
<span data-ttu-id="c8d84-132">Имя группы управления для определения политики, которую требуется обновить.</span><span class="sxs-lookup"><span data-stu-id="c8d84-132">The name of the management group of the policy set definition to update.</span></span>

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

### <span data-ttu-id="c8d84-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="c8d84-133">-Metadata</span></span>
<span data-ttu-id="c8d84-134">Метаданные определения обновленного набора политик.</span><span class="sxs-lookup"><span data-stu-id="c8d84-134">The metadata of the updated policy set definition.</span></span> <span data-ttu-id="c8d84-135">Это может быть либо путь к имени файла, содержащему метаданные, либо метаданные в виде строки.</span><span class="sxs-lookup"><span data-stu-id="c8d84-135">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="c8d84-136">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c8d84-136">-Name</span></span>
<span data-ttu-id="c8d84-137">Имя определения настройки политики.</span><span class="sxs-lookup"><span data-stu-id="c8d84-137">The policy set definition name.</span></span>

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

### <span data-ttu-id="c8d84-138">-Параметр</span><span class="sxs-lookup"><span data-stu-id="c8d84-138">-Parameter</span></span>
<span data-ttu-id="c8d84-139">Объявление параметров обновленного определения набора политик.</span><span class="sxs-lookup"><span data-stu-id="c8d84-139">The parameters declaration of the updated policy set definition.</span></span> <span data-ttu-id="c8d84-140">Это может быть путь к имени файла или универсальному коду ресурса (URI), содержащему объявление параметров, или объявление параметров в виде строки.</span><span class="sxs-lookup"><span data-stu-id="c8d84-140">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as a string.</span></span>

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

### <span data-ttu-id="c8d84-141">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c8d84-141">-PolicyDefinition</span></span>
<span data-ttu-id="c8d84-142">Определения политики.</span><span class="sxs-lookup"><span data-stu-id="c8d84-142">The policy definitions.</span></span> <span data-ttu-id="c8d84-143">Это может быть путь к имени файла, содержащему определения политики, или определениям политики в виде строки.</span><span class="sxs-lookup"><span data-stu-id="c8d84-143">This can either be a path to a file name containing the policy definitions, or the policy definitions as string.</span></span>

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

### <span data-ttu-id="c8d84-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="c8d84-144">-Pre</span></span>
<span data-ttu-id="c8d84-145">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="c8d84-145">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c8d84-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c8d84-146">-SubscriptionId</span></span>
<span data-ttu-id="c8d84-147">Идентификатор подписки для определения политики, которую требуется обновить.</span><span class="sxs-lookup"><span data-stu-id="c8d84-147">The subscription ID of the policy set definition to update.</span></span>

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

### <span data-ttu-id="c8d84-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c8d84-148">-Confirm</span></span>
<span data-ttu-id="c8d84-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c8d84-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8d84-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8d84-150">-WhatIf</span></span>
<span data-ttu-id="c8d84-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c8d84-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c8d84-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c8d84-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8d84-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8d84-153">CommonParameters</span></span>
<span data-ttu-id="c8d84-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c8d84-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8d84-155">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8d84-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8d84-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c8d84-156">INPUTS</span></span>

### <span data-ttu-id="c8d84-157">System. String</span><span class="sxs-lookup"><span data-stu-id="c8d84-157">System.String</span></span>

### <span data-ttu-id="c8d84-158">System. Nullable "1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c8d84-158">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="c8d84-159">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8d84-159">OUTPUTS</span></span>

### <span data-ttu-id="c8d84-160">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="c8d84-160">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c8d84-161">Пуск</span><span class="sxs-lookup"><span data-stu-id="c8d84-161">NOTES</span></span>

## <span data-ttu-id="c8d84-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c8d84-162">RELATED LINKS</span></span>
