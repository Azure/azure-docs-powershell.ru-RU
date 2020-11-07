---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAssignment.md
ms.openlocfilehash: e2cce15271b1289a2d6bfe5f8874f004ba95a04b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905630"
---
# <span data-ttu-id="e40db-101">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="e40db-101">Get-AzPolicyAssignment</span></span>

## <span data-ttu-id="e40db-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e40db-102">SYNOPSIS</span></span>
<span data-ttu-id="e40db-103">Получение назначений политики.</span><span class="sxs-lookup"><span data-stu-id="e40db-103">Gets policy assignments.</span></span>

## <span data-ttu-id="e40db-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e40db-104">SYNTAX</span></span>

### <span data-ttu-id="e40db-105">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e40db-105">DefaultParameterSet (Default)</span></span>
```
Get-AzPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e40db-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e40db-106">NameParameterSet</span></span>
```
Get-AzPolicyAssignment [-Name <String>] [-Scope <String>] [-PolicyDefinitionId <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e40db-107">IncludeDescendentParameterSet</span><span class="sxs-lookup"><span data-stu-id="e40db-107">IncludeDescendentParameterSet</span></span>
```
Get-AzPolicyAssignment [-Scope <String>] [-IncludeDescendent] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e40db-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e40db-108">IdParameterSet</span></span>
```
Get-AzPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e40db-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e40db-109">DESCRIPTION</span></span>
<span data-ttu-id="e40db-110">Командлет **Get-AzPolicyAssignment** получает все назначения политик или конкретные назначения.</span><span class="sxs-lookup"><span data-stu-id="e40db-110">The **Get-AzPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="e40db-111">Определите назначение политики для получения имени и области или по ИДЕНТИФИКАТОРу.</span><span class="sxs-lookup"><span data-stu-id="e40db-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="e40db-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e40db-112">EXAMPLES</span></span>

### <span data-ttu-id="e40db-113">Пример 1: получение всех назначений политики</span><span class="sxs-lookup"><span data-stu-id="e40db-113">Example 1: Get all policy assignments</span></span>
```
PS C:\> Get-AzPolicyAssignment
```

<span data-ttu-id="e40db-114">Эта команда получает все назначения политики.</span><span class="sxs-lookup"><span data-stu-id="e40db-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="e40db-115">Пример 2: получение определенного назначения политики</span><span class="sxs-lookup"><span data-stu-id="e40db-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="e40db-116">Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью командлета Get-AzResourceGroup и сохраняет его в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e40db-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="e40db-117">Вторая команда получает назначение политики с именем PolicyAssignment07 для области, которой идентифицировано свойство **ResourceId** для $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e40db-117">The second command gets the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

### <span data-ttu-id="e40db-118">Пример 3: получение всех назначений политики, назначенных группе управления</span><span class="sxs-lookup"><span data-stu-id="e40db-118">Example 3: Get all policy assignments assigned to a management group</span></span>
```
PS C:\> $mgId = 'myManagementGroup'
PS C:\> Get-AzPolicyAssignment -Scope '/providers/Microsoft.Management/managementgroups/$mgId'
```

<span data-ttu-id="e40db-119">Первая команда задает идентификатор группы управления для запроса.</span><span class="sxs-lookup"><span data-stu-id="e40db-119">The first command specifies the ID of the management group to query.</span></span>
<span data-ttu-id="e40db-120">Вторая команда получает все назначения политики, назначенные группе управления с ИДЕНТИФИКАТОРом "myManagementGroup".</span><span class="sxs-lookup"><span data-stu-id="e40db-120">The second command gets all of the policy assignments that are assigned to the management group with ID 'myManagementGroup'.</span></span>

## <span data-ttu-id="e40db-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e40db-121">PARAMETERS</span></span>

### <span data-ttu-id="e40db-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e40db-122">-ApiVersion</span></span>
<span data-ttu-id="e40db-123">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e40db-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="e40db-124">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="e40db-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="e40db-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e40db-125">-DefaultProfile</span></span>
<span data-ttu-id="e40db-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e40db-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e40db-127">-ID</span><span class="sxs-lookup"><span data-stu-id="e40db-127">-Id</span></span>
<span data-ttu-id="e40db-128">Указывает полный идентификатор ресурса для назначения политики, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e40db-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e40db-129">-IncludeDescendent</span><span class="sxs-lookup"><span data-stu-id="e40db-129">-IncludeDescendent</span></span>
<span data-ttu-id="e40db-130">Приводит к тому, что список возвращенных назначений политики включает в себя все задания, связанные с данной областью, в том числе из областей предков и из областей потомков.</span><span class="sxs-lookup"><span data-stu-id="e40db-130">Causes the list of returned policy assignments to include all assignments related to the given scope, including those from ancestor scopes and those from descendent scopes.</span></span>

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

### <span data-ttu-id="e40db-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e40db-131">-Name</span></span>
<span data-ttu-id="e40db-132">Указывает имя назначения политики, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e40db-132">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e40db-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="e40db-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="e40db-134">Указывает идентификатор определения политики для назначений политики, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e40db-134">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e40db-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="e40db-135">-Pre</span></span>
<span data-ttu-id="e40db-136">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="e40db-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e40db-137">-Scope</span><span class="sxs-lookup"><span data-stu-id="e40db-137">-Scope</span></span>
<span data-ttu-id="e40db-138">Указывает область, в которой применяется политика для задания, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e40db-138">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e40db-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e40db-139">CommonParameters</span></span>
<span data-ttu-id="e40db-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e40db-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e40db-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e40db-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e40db-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e40db-142">INPUTS</span></span>

### <span data-ttu-id="e40db-143">System. String</span><span class="sxs-lookup"><span data-stu-id="e40db-143">System.String</span></span>

### <span data-ttu-id="e40db-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e40db-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e40db-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e40db-145">OUTPUTS</span></span>

### <span data-ttu-id="e40db-146">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="e40db-146">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="e40db-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="e40db-147">NOTES</span></span>

## <span data-ttu-id="e40db-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e40db-148">RELATED LINKS</span></span>

[<span data-ttu-id="e40db-149">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="e40db-149">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="e40db-150">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="e40db-150">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="e40db-151">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="e40db-151">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


