---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
ms.openlocfilehash: 71f3c6ab80fd0ba44d715cb25b4bf690e44359c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560711"
---
# <span data-ttu-id="f36bc-101">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f36bc-101">Get-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="f36bc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f36bc-102">SYNOPSIS</span></span>
<span data-ttu-id="f36bc-103">Получение назначений политики.</span><span class="sxs-lookup"><span data-stu-id="f36bc-103">Gets policy assignments.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f36bc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f36bc-104">SYNTAX</span></span>

### <span data-ttu-id="f36bc-105">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f36bc-105">DefaultParameterSet (Default)</span></span>
```
Get-AzureRmPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f36bc-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f36bc-106">NameParameterSet</span></span>
```
Get-AzureRmPolicyAssignment [-Name <String>] [-Scope <String>] [-PolicyDefinitionId <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f36bc-107">IncludeDescendentParameterSet</span><span class="sxs-lookup"><span data-stu-id="f36bc-107">IncludeDescendentParameterSet</span></span>
```
Get-AzureRmPolicyAssignment [-Scope <String>] [-IncludeDescendent] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f36bc-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f36bc-108">IdParameterSet</span></span>
```
Get-AzureRmPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f36bc-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f36bc-109">DESCRIPTION</span></span>
<span data-ttu-id="f36bc-110">Командлет **Get-AzureRmPolicyAssignment** получает все назначения политик или конкретные назначения.</span><span class="sxs-lookup"><span data-stu-id="f36bc-110">The **Get-AzureRmPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="f36bc-111">Определите назначение политики для получения имени и области или по ИДЕНТИФИКАТОРу.</span><span class="sxs-lookup"><span data-stu-id="f36bc-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="f36bc-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f36bc-112">EXAMPLES</span></span>

### <span data-ttu-id="f36bc-113">Пример 1: получение всех назначений политики</span><span class="sxs-lookup"><span data-stu-id="f36bc-113">Example 1: Get all policy assignments</span></span>
```
PS C:\> Get-AzureRmPolicyAssignment
```

<span data-ttu-id="f36bc-114">Эта команда получает все назначения политики.</span><span class="sxs-lookup"><span data-stu-id="f36bc-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="f36bc-115">Пример 2: получение определенного назначения политики</span><span class="sxs-lookup"><span data-stu-id="f36bc-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> Get-AzureRmPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="f36bc-116">Первая команда получает группу ресурсов с именем ResourceGroup11, используя Get-AzureRMResourceGroup cmdletand сохраняет ее в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f36bc-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdletand stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="f36bc-117">Вторая команда получает назначение политики с именем PolicyAssignment07 для области, которой идентифицировано свойство **ResourceId** для $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f36bc-117">The second command gets the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

### <span data-ttu-id="f36bc-118">Пример 3: получение всех назначений политики, назначенных группе управления</span><span class="sxs-lookup"><span data-stu-id="f36bc-118">Example 3: Get all policy assignments assigned to a management group</span></span>
```
PS C:\> $mgId = 'myManagementGroup'
PS C:\> Get-AzureRmPolicyAssignment -Scope '/providers/Microsoft.Management/managementgroups/$mgId'
```

<span data-ttu-id="f36bc-119">Первая команда задает идентификатор группы управления для запроса.</span><span class="sxs-lookup"><span data-stu-id="f36bc-119">The first command specifies the ID of the management group to query.</span></span>
<span data-ttu-id="f36bc-120">Вторая команда получает все назначения политики, назначенные группе управления с ИДЕНТИФИКАТОРом "myManagementGroup".</span><span class="sxs-lookup"><span data-stu-id="f36bc-120">The second command gets all of the policy assignments that are assigned to the management group with ID 'myManagementGroup'.</span></span>

## <span data-ttu-id="f36bc-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f36bc-121">PARAMETERS</span></span>

### <span data-ttu-id="f36bc-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f36bc-122">-ApiVersion</span></span>
<span data-ttu-id="f36bc-123">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f36bc-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="f36bc-124">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="f36bc-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="f36bc-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f36bc-125">-DefaultProfile</span></span>
<span data-ttu-id="f36bc-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f36bc-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f36bc-127">-ID</span><span class="sxs-lookup"><span data-stu-id="f36bc-127">-Id</span></span>
<span data-ttu-id="f36bc-128">Указывает полный идентификатор ресурса для назначения политики, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f36bc-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f36bc-129">-IncludeDescendent</span><span class="sxs-lookup"><span data-stu-id="f36bc-129">-IncludeDescendent</span></span>
<span data-ttu-id="f36bc-130">Приводит к тому, что список возвращенных назначений политики включает в себя все задания, связанные с данной областью, в том числе из областей предков и из областей потомков.</span><span class="sxs-lookup"><span data-stu-id="f36bc-130">Causes the list of returned policy assignments to include all assignments related to the given scope, including those from ancestor scopes and those from descendent scopes.</span></span>

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

### <span data-ttu-id="f36bc-131">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f36bc-131">-InformationAction</span></span>
<span data-ttu-id="f36bc-132">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="f36bc-132">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="f36bc-133">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f36bc-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f36bc-134">Продолжал</span><span class="sxs-lookup"><span data-stu-id="f36bc-134">Continue</span></span>
- <span data-ttu-id="f36bc-135">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="f36bc-135">Ignore</span></span>
- <span data-ttu-id="f36bc-136">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="f36bc-136">Inquire</span></span>
- <span data-ttu-id="f36bc-137">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f36bc-137">SilentlyContinue</span></span>
- <span data-ttu-id="f36bc-138">Остановить</span><span class="sxs-lookup"><span data-stu-id="f36bc-138">Stop</span></span>
- <span data-ttu-id="f36bc-139">Рвать</span><span class="sxs-lookup"><span data-stu-id="f36bc-139">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f36bc-140">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f36bc-140">-InformationVariable</span></span>
<span data-ttu-id="f36bc-141">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="f36bc-141">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f36bc-142">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f36bc-142">-Name</span></span>
<span data-ttu-id="f36bc-143">Указывает имя назначения политики, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f36bc-143">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f36bc-144">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="f36bc-144">-PolicyDefinitionId</span></span>
<span data-ttu-id="f36bc-145">Указывает идентификатор определения политики для назначений политики, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f36bc-145">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f36bc-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="f36bc-146">-Pre</span></span>
<span data-ttu-id="f36bc-147">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="f36bc-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f36bc-148">-Scope</span><span class="sxs-lookup"><span data-stu-id="f36bc-148">-Scope</span></span>
<span data-ttu-id="f36bc-149">Указывает область, в которой применяется политика для задания, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f36bc-149">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f36bc-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f36bc-150">CommonParameters</span></span>
<span data-ttu-id="f36bc-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f36bc-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f36bc-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f36bc-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f36bc-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f36bc-153">INPUTS</span></span>

## <span data-ttu-id="f36bc-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f36bc-154">OUTPUTS</span></span>

## <span data-ttu-id="f36bc-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="f36bc-155">NOTES</span></span>

## <span data-ttu-id="f36bc-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f36bc-156">RELATED LINKS</span></span>

[<span data-ttu-id="f36bc-157">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f36bc-157">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="f36bc-158">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f36bc-158">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="f36bc-159">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f36bc-159">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


