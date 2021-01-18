---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
ms.openlocfilehash: 4ec965e63a779a5b0ebb606819e5e9f7f20b035e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505276"
---
# <span data-ttu-id="629df-101">Get-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="629df-101">Get-AzPolicySetDefinition</span></span>

## <span data-ttu-id="629df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="629df-102">SYNOPSIS</span></span>
<span data-ttu-id="629df-103">Получает определения набора политик.</span><span class="sxs-lookup"><span data-stu-id="629df-103">Gets policy set definitions.</span></span>

## <span data-ttu-id="629df-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="629df-104">SYNTAX</span></span>

### <span data-ttu-id="629df-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="629df-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="629df-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="629df-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="629df-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="629df-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="629df-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="629df-108">IdParameterSet</span></span>
```
Get-AzPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="629df-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="629df-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="629df-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="629df-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="629df-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="629df-111">DESCRIPTION</span></span>
<span data-ttu-id="629df-112">С **помощью cmdlet Get-AzPolicySetDefinition** можно получить набор определений набора политик или определение определенного набора, определенного по имени или коду.</span><span class="sxs-lookup"><span data-stu-id="629df-112">The **Get-AzPolicySetDefinition** cmdlet gets a collection of policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="629df-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="629df-113">EXAMPLES</span></span>

### <span data-ttu-id="629df-114">Пример 1. Получить все определения набора политик</span><span class="sxs-lookup"><span data-stu-id="629df-114">Example 1: Get all policy set definitions</span></span>
```
PS C:\> Get-AzPolicySetDefinition
```

<span data-ttu-id="629df-115">Эта команда получает все определения набора политик.</span><span class="sxs-lookup"><span data-stu-id="629df-115">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="629df-116">Пример 2. Определение набора политик из текущей подписки по имени</span><span class="sxs-lookup"><span data-stu-id="629df-116">Example 2: Get policy set definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition'
```

<span data-ttu-id="629df-117">Эта команда получает определение набора политик VMPolicySetDefinition из текущей подписки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="629df-117">This command gets the policy set definition named VMPolicySetDefinition from the current default subscription.</span></span>

### <span data-ttu-id="629df-118">Пример 3. Определение набора политик из подписки по имени</span><span class="sxs-lookup"><span data-stu-id="629df-118">Example 3: Get policy set definition from subscription by name</span></span>
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -subscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca'
```

<span data-ttu-id="629df-119">Эта команда получает определение политики VMPolicySetDefinition из подписки с ИД 3bf44b72-c631-427a-b8c8-53e2595398ca.</span><span class="sxs-lookup"><span data-stu-id="629df-119">This command gets the policy definition named VMPolicySetDefinition from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

### <span data-ttu-id="629df-120">Пример 4. Получить все определения настраиваемого набора политик из группы управления</span><span class="sxs-lookup"><span data-stu-id="629df-120">Example 4: Get all custom policy set definitions from management group</span></span>
```
PS C:\> Get-AzPolicySetDefinition -ManagementGroupName 'Dept42' -Custom
```

<span data-ttu-id="629df-121">Эта команда получает все определения настраиваемого набора политик из группы управления "Отдел42".</span><span class="sxs-lookup"><span data-stu-id="629df-121">This command gets all custom policy set definitions from the management group named Dept42.</span></span>

### <span data-ttu-id="629df-122">Пример 5. Получать определения набора политик из данной категории</span><span class="sxs-lookup"><span data-stu-id="629df-122">Example 5: Get policy set definitions from a given category</span></span>
```
PS C:\> Get-AzPolicySetDefinition | where-object {$_.Properties.metadata.category -eq "Virtual Machine"}
```

<span data-ttu-id="629df-123">Эта команда получает все определения набора политик в категории "Виртуальная машинка".</span><span class="sxs-lookup"><span data-stu-id="629df-123">This command gets all policy set definitions in category "Virtual Machine".</span></span>

## <span data-ttu-id="629df-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="629df-124">PARAMETERS</span></span>

### <span data-ttu-id="629df-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="629df-125">-ApiVersion</span></span>
<span data-ttu-id="629df-126">Указывает на версию API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="629df-126">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="629df-127">Если он не задан, версия API будет автоматически определена как наиболее последняя из доступных.</span><span class="sxs-lookup"><span data-stu-id="629df-127">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="629df-128">-Builtin</span><span class="sxs-lookup"><span data-stu-id="629df-128">-Builtin</span></span>
<span data-ttu-id="629df-129">Ограничивает список результатов только встроенными определениями наборов политик.</span><span class="sxs-lookup"><span data-stu-id="629df-129">Limits list of results to only built-in policy set definitions.</span></span>

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

### <span data-ttu-id="629df-130">-Custom</span><span class="sxs-lookup"><span data-stu-id="629df-130">-Custom</span></span>
<span data-ttu-id="629df-131">Список результатов ограничивается только определением настраиваемой политики.</span><span class="sxs-lookup"><span data-stu-id="629df-131">Limits list of results to only custom policy set definitions.</span></span>

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

### <span data-ttu-id="629df-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="629df-132">-DefaultProfile</span></span>
<span data-ttu-id="629df-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="629df-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="629df-134">-Id</span><span class="sxs-lookup"><span data-stu-id="629df-134">-Id</span></span>
<span data-ttu-id="629df-135">Полное определение набора политик, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="629df-135">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="629df-136">Например, /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="629df-136">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="629df-137">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="629df-137">-ManagementGroupName</span></span>
<span data-ttu-id="629df-138">Имя группы управления определениями наборов политик, которые нужно получить.</span><span class="sxs-lookup"><span data-stu-id="629df-138">The name of the management group of the policy set definition(s) to get.</span></span>

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

### <span data-ttu-id="629df-139">-Name</span><span class="sxs-lookup"><span data-stu-id="629df-139">-Name</span></span>
<span data-ttu-id="629df-140">Имя определения набора политики.</span><span class="sxs-lookup"><span data-stu-id="629df-140">The policy set definition name.</span></span>

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

### <span data-ttu-id="629df-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="629df-141">-Pre</span></span>
<span data-ttu-id="629df-142">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="629df-142">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="629df-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="629df-143">-SubscriptionId</span></span>
<span data-ttu-id="629df-144">ИД подписки для определений наборов политик, которые требуется получить.</span><span class="sxs-lookup"><span data-stu-id="629df-144">The subscription ID of the policy set definition(s) to get.</span></span>

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

### <span data-ttu-id="629df-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="629df-145">CommonParameters</span></span>
<span data-ttu-id="629df-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="629df-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="629df-147">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="629df-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="629df-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="629df-148">INPUTS</span></span>

### <span data-ttu-id="629df-149">System.String</span><span class="sxs-lookup"><span data-stu-id="629df-149">System.String</span></span>

### <span data-ttu-id="629df-150">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="629df-150">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="629df-151">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="629df-151">OUTPUTS</span></span>

### <span data-ttu-id="629df-152">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="629df-152">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="629df-153">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="629df-153">NOTES</span></span>

## <span data-ttu-id="629df-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="629df-154">RELATED LINKS</span></span>
