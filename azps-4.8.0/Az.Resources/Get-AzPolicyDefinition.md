---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyDefinition.md
ms.openlocfilehash: 52de80f1ad3cf84a7aa309b5e97b7fa24e9419b8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244221"
---
# <span data-ttu-id="422b7-101">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="422b7-101">Get-AzPolicyDefinition</span></span>

## <span data-ttu-id="422b7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="422b7-102">SYNOPSIS</span></span>
<span data-ttu-id="422b7-103">Получение определений политики.</span><span class="sxs-lookup"><span data-stu-id="422b7-103">Gets policy definitions.</span></span>

## <span data-ttu-id="422b7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="422b7-104">SYNTAX</span></span>

### <span data-ttu-id="422b7-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="422b7-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicyDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="422b7-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="422b7-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="422b7-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="422b7-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="422b7-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="422b7-108">IdParameterSet</span></span>
```
Get-AzPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="422b7-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="422b7-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="422b7-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="422b7-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="422b7-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="422b7-111">DESCRIPTION</span></span>
<span data-ttu-id="422b7-112">Командлет **Get-AzPolicyDefinition** получает коллекцию определений политик или определенное определение политики, определяемое именем или идентификатором.</span><span class="sxs-lookup"><span data-stu-id="422b7-112">The **Get-AzPolicyDefinition** cmdlet gets a collection of policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="422b7-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="422b7-113">EXAMPLES</span></span>

### <span data-ttu-id="422b7-114">Пример 1: получение всех определений политик</span><span class="sxs-lookup"><span data-stu-id="422b7-114">Example 1: Get all policy definitions</span></span>
```
PS C:\> Get-AzPolicyDefinition
```

<span data-ttu-id="422b7-115">Эта команда получает все определения политики.</span><span class="sxs-lookup"><span data-stu-id="422b7-115">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="422b7-116">Пример 2: получение определения политики из текущей подписки по имени</span><span class="sxs-lookup"><span data-stu-id="422b7-116">Example 2: Get policy definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="422b7-117">Эта команда получает определение политики с именем VMPolicyDefinition из текущей подписки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="422b7-117">This command gets the policy definition named VMPolicyDefinition from the current default subscription.</span></span>

### <span data-ttu-id="422b7-118">Пример 3: получение определения политики из группы управления по имени</span><span class="sxs-lookup"><span data-stu-id="422b7-118">Example 3: Get policy definition from management group by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName 'Dept42'
```

<span data-ttu-id="422b7-119">Эта команда получает определение политики с именем VMPolicyDefinition из группы управления с именем Dept42.</span><span class="sxs-lookup"><span data-stu-id="422b7-119">This command gets the policy definition named VMPolicyDefinition from the management group named Dept42.</span></span>

### <span data-ttu-id="422b7-120">Пример 4: получение всех встроенных определений политик из подписки</span><span class="sxs-lookup"><span data-stu-id="422b7-120">Example 4: Get all built-in policy definitions from subscription</span></span>
```
PS C:\> Get-AzPolicyDefinition -SubscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca' -Builtin
```

<span data-ttu-id="422b7-121">Эта команда получает все встроенные определения политик из подписки с ИДЕНТИФИКАТОРом 3bf44b72-c631-427a-b8c8-53e2595398ca.</span><span class="sxs-lookup"><span data-stu-id="422b7-121">This command gets all built-in policy definitions from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

### <span data-ttu-id="422b7-122">Пример 5: получение определений политики из определенной категории</span><span class="sxs-lookup"><span data-stu-id="422b7-122">Example 5: Get policy definitions from a given category</span></span>
```
PS C:\> Get-AzPolicyDefinition | where-object {$_.Properties.metadata.category -eq "Virtual Machine"}
```

<span data-ttu-id="422b7-123">Эта команда получает все определения политик в категории "виртуальная машина".</span><span class="sxs-lookup"><span data-stu-id="422b7-123">This command gets all policy definitions in category "Virtual Machine".</span></span>

## <span data-ttu-id="422b7-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="422b7-124">PARAMETERS</span></span>

### <span data-ttu-id="422b7-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="422b7-125">-ApiVersion</span></span>
<span data-ttu-id="422b7-126">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="422b7-126">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="422b7-127">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="422b7-127">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="422b7-128">-Builtin</span><span class="sxs-lookup"><span data-stu-id="422b7-128">-Builtin</span></span>
<span data-ttu-id="422b7-129">Ограничивает список результатов только встроенными определениями политик.</span><span class="sxs-lookup"><span data-stu-id="422b7-129">Limits list of results to only built-in policy definitions.</span></span>

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

### <span data-ttu-id="422b7-130">-Custom</span><span class="sxs-lookup"><span data-stu-id="422b7-130">-Custom</span></span>
<span data-ttu-id="422b7-131">Ограничивает список результатов только пользовательскими определениями политик.</span><span class="sxs-lookup"><span data-stu-id="422b7-131">Limits list of results to only custom policy definitions.</span></span>

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

### <span data-ttu-id="422b7-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="422b7-132">-DefaultProfile</span></span>
<span data-ttu-id="422b7-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="422b7-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="422b7-134">-ID</span><span class="sxs-lookup"><span data-stu-id="422b7-134">-Id</span></span>
<span data-ttu-id="422b7-135">Указывает полный идентификатор ресурса для определения политики, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="422b7-135">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="422b7-136">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="422b7-136">-ManagementGroupName</span></span>
<span data-ttu-id="422b7-137">Имя группы управления для определений политик, которые требуется получить.</span><span class="sxs-lookup"><span data-stu-id="422b7-137">The name of the management group of the policy definition(s) to get.</span></span>

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

### <span data-ttu-id="422b7-138">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="422b7-138">-Name</span></span>
<span data-ttu-id="422b7-139">Указывает имя определения политики, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="422b7-139">Specifies the name of the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="422b7-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="422b7-140">-Pre</span></span>
<span data-ttu-id="422b7-141">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="422b7-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="422b7-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="422b7-142">-SubscriptionId</span></span>
<span data-ttu-id="422b7-143">Идентификатор подписки определений политик, которые требуется получить.</span><span class="sxs-lookup"><span data-stu-id="422b7-143">The subscription ID of the policy definition(s) to get.</span></span>

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

### <span data-ttu-id="422b7-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="422b7-144">CommonParameters</span></span>
<span data-ttu-id="422b7-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="422b7-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="422b7-146">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="422b7-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="422b7-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="422b7-147">INPUTS</span></span>

### <span data-ttu-id="422b7-148">System. String</span><span class="sxs-lookup"><span data-stu-id="422b7-148">System.String</span></span>

### <span data-ttu-id="422b7-149">System. Nullable "1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="422b7-149">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="422b7-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="422b7-150">OUTPUTS</span></span>

### <span data-ttu-id="422b7-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="422b7-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="422b7-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="422b7-152">NOTES</span></span>

## <span data-ttu-id="422b7-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="422b7-153">RELATED LINKS</span></span>

[<span data-ttu-id="422b7-154">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="422b7-154">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="422b7-155">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="422b7-155">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

[<span data-ttu-id="422b7-156">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="422b7-156">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)

