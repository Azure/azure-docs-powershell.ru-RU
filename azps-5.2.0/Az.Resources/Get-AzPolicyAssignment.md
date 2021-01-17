---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAssignment.md
ms.openlocfilehash: 4d5b230b741deec10daa44dab7e4faa44ac96b61
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397919"
---
# <span data-ttu-id="669ae-101">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="669ae-101">Get-AzPolicyAssignment</span></span>

## <span data-ttu-id="669ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="669ae-102">SYNOPSIS</span></span>
<span data-ttu-id="669ae-103">Получает назначения политик.</span><span class="sxs-lookup"><span data-stu-id="669ae-103">Gets policy assignments.</span></span>

## <span data-ttu-id="669ae-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="669ae-104">SYNTAX</span></span>

### <span data-ttu-id="669ae-105">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="669ae-105">DefaultParameterSet (Default)</span></span>
```
Get-AzPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="669ae-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="669ae-106">NameParameterSet</span></span>
```
Get-AzPolicyAssignment [-Name <String>] [-Scope <String>] [-PolicyDefinitionId <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="669ae-107">IncludeDescendentParameterSet</span><span class="sxs-lookup"><span data-stu-id="669ae-107">IncludeDescendentParameterSet</span></span>
```
Get-AzPolicyAssignment [-Scope <String>] [-IncludeDescendent] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="669ae-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="669ae-108">IdParameterSet</span></span>
```
Get-AzPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="669ae-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="669ae-109">DESCRIPTION</span></span>
<span data-ttu-id="669ae-110">Для получения всех назначений политики или определенных назначений будет выполняться **cmdlet Get-AzPolicyAssignment.**</span><span class="sxs-lookup"><span data-stu-id="669ae-110">The **Get-AzPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="669ae-111">Определите назначение политики, которое нужно получить по имени, области или по ИД.</span><span class="sxs-lookup"><span data-stu-id="669ae-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="669ae-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="669ae-112">EXAMPLES</span></span>

### <span data-ttu-id="669ae-113">Пример 1. Получить все назначения политики</span><span class="sxs-lookup"><span data-stu-id="669ae-113">Example 1: Get all policy assignments</span></span>
```
PS C:\> Get-AzPolicyAssignment
```

<span data-ttu-id="669ae-114">Эта команда получает все назначения политики.</span><span class="sxs-lookup"><span data-stu-id="669ae-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="669ae-115">Пример 2. Получить определенное назначение политики</span><span class="sxs-lookup"><span data-stu-id="669ae-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="669ae-116">Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью Get-AzResourceGroup и сохраняет ее в $ResourceGroup переменной.</span><span class="sxs-lookup"><span data-stu-id="669ae-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="669ae-117">Вторая команда получает назначение политики PolicyAssignment07 для области, которую определяет свойство **ResourceId,** $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="669ae-117">The second command gets the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

### <span data-ttu-id="669ae-118">Пример 3. Назначение всех назначений политики группе управления</span><span class="sxs-lookup"><span data-stu-id="669ae-118">Example 3: Get all policy assignments assigned to a management group</span></span>
```
PS C:\> $mgId = 'myManagementGroup'
PS C:\> Get-AzPolicyAssignment -Scope '/providers/Microsoft.Management/managementgroups/$mgId'
```

<span data-ttu-id="669ae-119">Первая команда определяет ИД группы управления для запроса.</span><span class="sxs-lookup"><span data-stu-id="669ae-119">The first command specifies the ID of the management group to query.</span></span>
<span data-ttu-id="669ae-120">Вторая команда получает все назначения политики, которые назначены группе управления с ИД "myManagementGroup".</span><span class="sxs-lookup"><span data-stu-id="669ae-120">The second command gets all of the policy assignments that are assigned to the management group with ID 'myManagementGroup'.</span></span>

## <span data-ttu-id="669ae-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="669ae-121">PARAMETERS</span></span>

### <span data-ttu-id="669ae-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="669ae-122">-ApiVersion</span></span>
<span data-ttu-id="669ae-123">Определяет версию API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="669ae-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="669ae-124">Если не указать версию, этот cmdlet использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="669ae-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="669ae-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="669ae-125">-DefaultProfile</span></span>
<span data-ttu-id="669ae-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="669ae-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="669ae-127">-Id</span><span class="sxs-lookup"><span data-stu-id="669ae-127">-Id</span></span>
<span data-ttu-id="669ae-128">Определяет полностью определенный код ресурса для назначения политики, которое получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="669ae-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="669ae-129">-IncludeDescendent</span><span class="sxs-lookup"><span data-stu-id="669ae-129">-IncludeDescendent</span></span>
<span data-ttu-id="669ae-130">Приводит к включению в список возвращаемого назначения политики всех назначений, связанных с заданной областью, в том числе из областей предшественника и из областей по убытию.</span><span class="sxs-lookup"><span data-stu-id="669ae-130">Causes the list of returned policy assignments to include all assignments related to the given scope, including those from ancestor scopes and those from descendent scopes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: IncludeDescendentParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="669ae-131">-Name</span><span class="sxs-lookup"><span data-stu-id="669ae-131">-Name</span></span>
<span data-ttu-id="669ae-132">Указывает имя назначения политики, которое получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="669ae-132">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="669ae-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="669ae-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="669ae-134">Определяет код определения политики для назначений политики, которые получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="669ae-134">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, IdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="669ae-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="669ae-135">-Pre</span></span>
<span data-ttu-id="669ae-136">Указывает на то, что этот cmdlet рассматривает предварительные версии API при автоматическом определении используемой версии.</span><span class="sxs-lookup"><span data-stu-id="669ae-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="669ae-137">-Scope</span><span class="sxs-lookup"><span data-stu-id="669ae-137">-Scope</span></span>
<span data-ttu-id="669ae-138">Определяет область применения политики для назначения, которое получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="669ae-138">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, IncludeDescendentParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="669ae-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="669ae-139">CommonParameters</span></span>
<span data-ttu-id="669ae-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="669ae-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="669ae-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="669ae-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="669ae-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="669ae-142">INPUTS</span></span>

### <span data-ttu-id="669ae-143">System.String</span><span class="sxs-lookup"><span data-stu-id="669ae-143">System.String</span></span>

### <span data-ttu-id="669ae-144">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="669ae-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="669ae-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="669ae-145">OUTPUTS</span></span>

### <span data-ttu-id="669ae-146">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="669ae-146">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="669ae-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="669ae-147">NOTES</span></span>

## <span data-ttu-id="669ae-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="669ae-148">RELATED LINKS</span></span>

[<span data-ttu-id="669ae-149">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="669ae-149">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="669ae-150">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="669ae-150">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="669ae-151">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="669ae-151">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


