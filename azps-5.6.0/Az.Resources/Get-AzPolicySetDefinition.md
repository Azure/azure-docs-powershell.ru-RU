---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
ms.openlocfilehash: 9ea6f37d21d35736116b2e9bf4fc3fcf20becf10
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973555"
---
# <span data-ttu-id="49506-101">Get-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="49506-101">Get-AzPolicySetDefinition</span></span>

## <span data-ttu-id="49506-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49506-102">SYNOPSIS</span></span>
<span data-ttu-id="49506-103">Получает определения набора политик.</span><span class="sxs-lookup"><span data-stu-id="49506-103">Gets policy set definitions.</span></span>

## <span data-ttu-id="49506-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="49506-104">SYNTAX</span></span>

### <span data-ttu-id="49506-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="49506-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49506-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="49506-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49506-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="49506-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49506-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="49506-108">IdParameterSet</span></span>
```
Get-AzPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="49506-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="49506-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49506-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="49506-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49506-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="49506-111">DESCRIPTION</span></span>
<span data-ttu-id="49506-112">С **помощью cmdlet Get-AzPolicySetDefinition** можно получить набор определений набора политик или определение, задаваемого по имени или коду.</span><span class="sxs-lookup"><span data-stu-id="49506-112">The **Get-AzPolicySetDefinition** cmdlet gets a collection of policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="49506-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="49506-113">EXAMPLES</span></span>

### <span data-ttu-id="49506-114">Пример 1. Получить все определения набора политик</span><span class="sxs-lookup"><span data-stu-id="49506-114">Example 1: Get all policy set definitions</span></span>
```
PS C:\> Get-AzPolicySetDefinition
```

<span data-ttu-id="49506-115">Эта команда получает все определения набора политик.</span><span class="sxs-lookup"><span data-stu-id="49506-115">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="49506-116">Пример 2. Определение набора политик из текущей подписки по имени</span><span class="sxs-lookup"><span data-stu-id="49506-116">Example 2: Get policy set definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition'
```

<span data-ttu-id="49506-117">Эта команда получает определение набора политик VMPolicySetDefinition из текущей подписки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="49506-117">This command gets the policy set definition named VMPolicySetDefinition from the current default subscription.</span></span>

### <span data-ttu-id="49506-118">Пример 3. Определение набора политик из подписки по имени</span><span class="sxs-lookup"><span data-stu-id="49506-118">Example 3: Get policy set definition from subscription by name</span></span>
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -subscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca'
```

<span data-ttu-id="49506-119">Эта команда получает определение политики VMPolicySetDefinition из подписки с ИД 3bf44b72-c631-427a-b8c8-53e2595398ca.</span><span class="sxs-lookup"><span data-stu-id="49506-119">This command gets the policy definition named VMPolicySetDefinition from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

### <span data-ttu-id="49506-120">Пример 4. Получить все определения настраиваемого набора политик из группы управления</span><span class="sxs-lookup"><span data-stu-id="49506-120">Example 4: Get all custom policy set definitions from management group</span></span>
```
PS C:\> Get-AzPolicySetDefinition -ManagementGroupName 'Dept42' -Custom
```

<span data-ttu-id="49506-121">Эта команда получает все определения настраиваемого набора политик из группы управления "Отдел42".</span><span class="sxs-lookup"><span data-stu-id="49506-121">This command gets all custom policy set definitions from the management group named Dept42.</span></span>

### <span data-ttu-id="49506-122">Пример 5. Получать определения набора политик из данной категории</span><span class="sxs-lookup"><span data-stu-id="49506-122">Example 5: Get policy set definitions from a given category</span></span>
```
PS C:\> Get-AzPolicySetDefinition | where-object {$_.Properties.metadata.category -eq "Virtual Machine"}
```

<span data-ttu-id="49506-123">Эта команда получает все определения набора политик в категории "Виртуальная машинка".</span><span class="sxs-lookup"><span data-stu-id="49506-123">This command gets all policy set definitions in category "Virtual Machine".</span></span>

## <span data-ttu-id="49506-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49506-124">PARAMETERS</span></span>

### <span data-ttu-id="49506-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="49506-125">-ApiVersion</span></span>
<span data-ttu-id="49506-126">Указывает версию API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="49506-126">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="49506-127">Если он не задан, версия API будет автоматически определена как наиболее последняя из доступных.</span><span class="sxs-lookup"><span data-stu-id="49506-127">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="49506-128">-Builtin</span><span class="sxs-lookup"><span data-stu-id="49506-128">-Builtin</span></span>
<span data-ttu-id="49506-129">Ограничивает список результатов только встроенными определениями наборов политик.</span><span class="sxs-lookup"><span data-stu-id="49506-129">Limits list of results to only built-in policy set definitions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BuiltinFilterParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49506-130">-Custom</span><span class="sxs-lookup"><span data-stu-id="49506-130">-Custom</span></span>
<span data-ttu-id="49506-131">Список результатов ограничивается только определением настраиваемой политики.</span><span class="sxs-lookup"><span data-stu-id="49506-131">Limits list of results to only custom policy set definitions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CustomFilterParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49506-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49506-132">-DefaultProfile</span></span>
<span data-ttu-id="49506-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="49506-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="49506-134">-Id</span><span class="sxs-lookup"><span data-stu-id="49506-134">-Id</span></span>
<span data-ttu-id="49506-135">Полное определение набора политик, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="49506-135">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="49506-136">Например, /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="49506-136">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="49506-137">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="49506-137">-ManagementGroupName</span></span>
<span data-ttu-id="49506-138">Имя группы управления определениями наборов политик, которые нужно получить.</span><span class="sxs-lookup"><span data-stu-id="49506-138">The name of the management group of the policy set definition(s) to get.</span></span>

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

```yaml
Type: System.String
Parameter Sets: BuiltinFilterParameterSet, CustomFilterParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49506-139">-Name</span><span class="sxs-lookup"><span data-stu-id="49506-139">-Name</span></span>
<span data-ttu-id="49506-140">Имя определения набора политики.</span><span class="sxs-lookup"><span data-stu-id="49506-140">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49506-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="49506-141">-Pre</span></span>
<span data-ttu-id="49506-142">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="49506-142">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="49506-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="49506-143">-SubscriptionId</span></span>
<span data-ttu-id="49506-144">ИД подписки для определений наборов политик, которые требуется получить.</span><span class="sxs-lookup"><span data-stu-id="49506-144">The subscription ID of the policy set definition(s) to get.</span></span>

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

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: BuiltinFilterParameterSet, CustomFilterParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49506-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49506-145">CommonParameters</span></span>
<span data-ttu-id="49506-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49506-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49506-147">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49506-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49506-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="49506-148">INPUTS</span></span>

### <span data-ttu-id="49506-149">System.String</span><span class="sxs-lookup"><span data-stu-id="49506-149">System.String</span></span>

### <span data-ttu-id="49506-150">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="49506-150">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="49506-151">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="49506-151">OUTPUTS</span></span>

### <span data-ttu-id="49506-152">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="49506-152">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="49506-153">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="49506-153">NOTES</span></span>

## <span data-ttu-id="49506-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="49506-154">RELATED LINKS</span></span>
