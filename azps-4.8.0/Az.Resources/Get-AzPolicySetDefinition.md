---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
ms.openlocfilehash: 4ec965e63a779a5b0ebb606819e5e9f7f20b035e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077669"
---
# <span data-ttu-id="050c5-101">Get-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="050c5-101">Get-AzPolicySetDefinition</span></span>

## <span data-ttu-id="050c5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="050c5-102">SYNOPSIS</span></span>
<span data-ttu-id="050c5-103">Получение определений политики.</span><span class="sxs-lookup"><span data-stu-id="050c5-103">Gets policy set definitions.</span></span>

## <span data-ttu-id="050c5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="050c5-104">SYNTAX</span></span>

### <span data-ttu-id="050c5-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="050c5-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="050c5-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="050c5-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="050c5-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="050c5-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="050c5-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="050c5-108">IdParameterSet</span></span>
```
Get-AzPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="050c5-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="050c5-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="050c5-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="050c5-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="050c5-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="050c5-111">DESCRIPTION</span></span>
<span data-ttu-id="050c5-112">Командлет **Get-AzPolicySetDefinition** получает коллекцию определений политик или определенную определенную политику, определяемую именем или идентификатором.</span><span class="sxs-lookup"><span data-stu-id="050c5-112">The **Get-AzPolicySetDefinition** cmdlet gets a collection of policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="050c5-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="050c5-113">EXAMPLES</span></span>

### <span data-ttu-id="050c5-114">Пример 1: получение определений всех наборов политик</span><span class="sxs-lookup"><span data-stu-id="050c5-114">Example 1: Get all policy set definitions</span></span>
```
PS C:\> Get-AzPolicySetDefinition
```

<span data-ttu-id="050c5-115">Эта команда получает все определения политики.</span><span class="sxs-lookup"><span data-stu-id="050c5-115">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="050c5-116">Пример 2: получение определения политики из текущей подписки по имени</span><span class="sxs-lookup"><span data-stu-id="050c5-116">Example 2: Get policy set definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition'
```

<span data-ttu-id="050c5-117">Эта команда получает определение политики с именем VMPolicySetDefinition из текущей подписки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="050c5-117">This command gets the policy set definition named VMPolicySetDefinition from the current default subscription.</span></span>

### <span data-ttu-id="050c5-118">Пример 3: получение определения политики из подписки по имени</span><span class="sxs-lookup"><span data-stu-id="050c5-118">Example 3: Get policy set definition from subscription by name</span></span>
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -subscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca'
```

<span data-ttu-id="050c5-119">Эта команда получает определение политики с именем VMPolicySetDefinition из подписки с ИДЕНТИФИКАТОРом 3bf44b72-c631-427a-b8c8-53e2595398ca.</span><span class="sxs-lookup"><span data-stu-id="050c5-119">This command gets the policy definition named VMPolicySetDefinition from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

### <span data-ttu-id="050c5-120">Пример 4: получение всех настраиваемых определений политики из группы управления</span><span class="sxs-lookup"><span data-stu-id="050c5-120">Example 4: Get all custom policy set definitions from management group</span></span>
```
PS C:\> Get-AzPolicySetDefinition -ManagementGroupName 'Dept42' -Custom
```

<span data-ttu-id="050c5-121">Эта команда получает определения всех настраиваемых наборов политик из группы управления с именем Dept42.</span><span class="sxs-lookup"><span data-stu-id="050c5-121">This command gets all custom policy set definitions from the management group named Dept42.</span></span>

### <span data-ttu-id="050c5-122">Пример 5: получение определений политики из определенной категории</span><span class="sxs-lookup"><span data-stu-id="050c5-122">Example 5: Get policy set definitions from a given category</span></span>
```
PS C:\> Get-AzPolicySetDefinition | where-object {$_.Properties.metadata.category -eq "Virtual Machine"}
```

<span data-ttu-id="050c5-123">Эта команда получает определения всех наборов политик в категории "виртуальная машина".</span><span class="sxs-lookup"><span data-stu-id="050c5-123">This command gets all policy set definitions in category "Virtual Machine".</span></span>

## <span data-ttu-id="050c5-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="050c5-124">PARAMETERS</span></span>

### <span data-ttu-id="050c5-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="050c5-125">-ApiVersion</span></span>
<span data-ttu-id="050c5-126">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="050c5-126">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="050c5-127">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="050c5-127">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="050c5-128">-Builtin</span><span class="sxs-lookup"><span data-stu-id="050c5-128">-Builtin</span></span>
<span data-ttu-id="050c5-129">Ограничивает список результатов только встроенными определениями политик.</span><span class="sxs-lookup"><span data-stu-id="050c5-129">Limits list of results to only built-in policy set definitions.</span></span>

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

### <span data-ttu-id="050c5-130">-Custom</span><span class="sxs-lookup"><span data-stu-id="050c5-130">-Custom</span></span>
<span data-ttu-id="050c5-131">Ограничивает список результатов только настраиваемыми определениями политик.</span><span class="sxs-lookup"><span data-stu-id="050c5-131">Limits list of results to only custom policy set definitions.</span></span>

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

### <span data-ttu-id="050c5-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="050c5-132">-DefaultProfile</span></span>
<span data-ttu-id="050c5-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="050c5-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="050c5-134">-ID</span><span class="sxs-lookup"><span data-stu-id="050c5-134">-Id</span></span>
<span data-ttu-id="050c5-135">Полный идентификатор определения политики, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="050c5-135">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="050c5-136">Например,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="050c5-136">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="050c5-137">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="050c5-137">-ManagementGroupName</span></span>
<span data-ttu-id="050c5-138">Имя группы управления для определения политики, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="050c5-138">The name of the management group of the policy set definition(s) to get.</span></span>

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

### <span data-ttu-id="050c5-139">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="050c5-139">-Name</span></span>
<span data-ttu-id="050c5-140">Имя определения настройки политики.</span><span class="sxs-lookup"><span data-stu-id="050c5-140">The policy set definition name.</span></span>

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

### <span data-ttu-id="050c5-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="050c5-141">-Pre</span></span>
<span data-ttu-id="050c5-142">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="050c5-142">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="050c5-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="050c5-143">-SubscriptionId</span></span>
<span data-ttu-id="050c5-144">Идентификатор подписки определений политики, которые требуется получить.</span><span class="sxs-lookup"><span data-stu-id="050c5-144">The subscription ID of the policy set definition(s) to get.</span></span>

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

### <span data-ttu-id="050c5-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="050c5-145">CommonParameters</span></span>
<span data-ttu-id="050c5-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="050c5-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="050c5-147">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="050c5-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="050c5-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="050c5-148">INPUTS</span></span>

### <span data-ttu-id="050c5-149">System. String</span><span class="sxs-lookup"><span data-stu-id="050c5-149">System.String</span></span>

### <span data-ttu-id="050c5-150">System. Nullable "1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="050c5-150">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="050c5-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="050c5-151">OUTPUTS</span></span>

### <span data-ttu-id="050c5-152">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="050c5-152">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="050c5-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="050c5-153">NOTES</span></span>

## <span data-ttu-id="050c5-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="050c5-154">RELATED LINKS</span></span>
