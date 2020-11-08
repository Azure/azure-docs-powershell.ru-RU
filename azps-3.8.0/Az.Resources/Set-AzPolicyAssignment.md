---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
ms.openlocfilehash: ab0617b4012ca623bf67471a9a5bcc3ccf54d905
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066206"
---
# <span data-ttu-id="19115-101">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="19115-101">Set-AzPolicyAssignment</span></span>

## <span data-ttu-id="19115-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="19115-102">SYNOPSIS</span></span>
<span data-ttu-id="19115-103">Изменение назначения политики.</span><span class="sxs-lookup"><span data-stu-id="19115-103">Modifies a policy assignment.</span></span>

## <span data-ttu-id="19115-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="19115-104">SYNTAX</span></span>

### <span data-ttu-id="19115-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="19115-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19115-106">PolicyParameterNameObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="19115-106">PolicyParameterNameObjectParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity]
 [-Location <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19115-107">PolicyParameterNameStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="19115-107">PolicyParameterNameStringParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19115-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="19115-108">IdParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19115-109">PolicyParameterIdObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="19115-109">PolicyParameterIdObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19115-110">PolicyParameterIdStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="19115-110">PolicyParameterIdStringParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19115-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="19115-111">DESCRIPTION</span></span>
<span data-ttu-id="19115-112">Командлет **Set-AzPolicyAssignment** изменяет назначение политики.</span><span class="sxs-lookup"><span data-stu-id="19115-112">The **Set-AzPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="19115-113">Укажите назначение по ИДЕНТИФИКАТОРу или по имени и области.</span><span class="sxs-lookup"><span data-stu-id="19115-113">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="19115-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="19115-114">EXAMPLES</span></span>

### <span data-ttu-id="19115-115">Пример 1: обновление отображаемого имени</span><span class="sxs-lookup"><span data-stu-id="19115-115">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="19115-116">Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью командлета Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="19115-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="19115-117">Команда сохраняет этот объект в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="19115-117">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="19115-118">Вторая команда получает назначение политики с именем PolicyAssignment с помощью командлета Get-AzPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="19115-118">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="19115-119">Команда сохраняет этот объект в переменной $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="19115-119">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="19115-120">Последняя команда обновляет отображаемое имя в назначении политики для группы ресурсов, определяемой свойством **ResourceId** для $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="19115-120">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="19115-121">Пример 2: Добавление управляемого удостоверения в назначение политики</span><span class="sxs-lookup"><span data-stu-id="19115-121">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="19115-122">Первая команда получает назначение политики с именем PolicyAssignment из текущей подписки с помощью командлета Get-AzPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="19115-122">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="19115-123">Команда сохраняет этот объект в переменной $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="19115-123">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="19115-124">Последняя команда назначает управляемое удостоверение для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="19115-124">The final command assigns a managed identity to the policy assignment.</span></span>

### <span data-ttu-id="19115-125">Пример 3: Обновление параметров назначения политики с помощью нового объекта параметра политики</span><span class="sxs-lookup"><span data-stu-id="19115-125">Example 3: Update policy assignment parameters with new policy parameter object</span></span>
```
PS C:\> $Locations = Get-AzLocation | where {($_.displayname -like 'france*') -or ($_.displayname -like 'uk*')}
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="19115-126">Первая и вторая команды создают объект, содержащий все регионы Azure, имена которых начинаются с "Франция" или "Великобритания".</span><span class="sxs-lookup"><span data-stu-id="19115-126">The first and second commands create an object containing all Azure regions whose names start with "france" or "uk".</span></span>
<span data-ttu-id="19115-127">Вторая команда сохраняет этот объект в переменной $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="19115-127">The second command stores that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="19115-128">Третья команда получает назначение политики с именем "PolicyAssignment" команда сохраняет этот объект в переменной $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="19115-128">The third command gets the policy assignment named 'PolicyAssignment' The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="19115-129">Последняя команда обновляет значения параметров для назначения политики с именем PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="19115-129">The final command updates the parameter values on the policy assignment named PolicyAssignment.</span></span>

### <span data-ttu-id="19115-130">Пример 4: Обновление параметров назначения политики с помощью файла параметров политики</span><span class="sxs-lookup"><span data-stu-id="19115-130">Example 4: Update policy assignment parameters with policy parameter file</span></span>
<span data-ttu-id="19115-131">Создайте файл с именем _AllowedLocations.js_ в локальном рабочем каталоге со следующим содержимым.</span><span class="sxs-lookup"><span data-stu-id="19115-131">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

```
{
    "listOfAllowedLocations":  {
      "value": [
        "uksouth",
        "ukwest",
        "francecentral",
        "francesouth"
      ]
    }
}
```

```
PS C:\> Set-AzPolicyAssignment -Name 'PolicyAssignment' -PolicyParameter .\AllowedLocations.json
```

<span data-ttu-id="19115-132">Команда обновляет назначение политики с именем "PolicyAssignment" с помощью файла параметров политики, AllowedLocations.jsс локального рабочего каталога.</span><span class="sxs-lookup"><span data-stu-id="19115-132">The command updates the policy assignment named 'PolicyAssignment' using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="19115-133">Пример 5: обновление enforcementMode</span><span class="sxs-lookup"><span data-stu-id="19115-133">Example 5: Update an enforcementMode</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -EnforcementMode Default
```

<span data-ttu-id="19115-134">Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью командлета Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="19115-134">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="19115-135">Команда сохраняет этот объект в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="19115-135">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="19115-136">Вторая команда получает назначение политики с именем PolicyAssignment с помощью командлета Get-AzPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="19115-136">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="19115-137">Команда сохраняет этот объект в переменной $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="19115-137">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="19115-138">Последняя команда обновляет свойство enforcementMode в назначении политики для группы ресурсов, определяемой свойством **ResourceId** для $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="19115-138">The final command updates the enforcementMode property on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

## <span data-ttu-id="19115-139">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="19115-139">PARAMETERS</span></span>

### <span data-ttu-id="19115-140">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="19115-140">-ApiVersion</span></span>
<span data-ttu-id="19115-141">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="19115-141">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="19115-142">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="19115-142">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="19115-143">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="19115-143">-AssignIdentity</span></span>
<span data-ttu-id="19115-144">Создание и назначение удостоверения Azure Active Directory для этого назначения политики.</span><span class="sxs-lookup"><span data-stu-id="19115-144">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="19115-145">Удостоверение будет использоваться при выполнении развертываний для политик "deployIfNotExists".</span><span class="sxs-lookup"><span data-stu-id="19115-145">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="19115-146">При назначении удостоверения требуется указать расположение.</span><span class="sxs-lookup"><span data-stu-id="19115-146">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="19115-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19115-147">-DefaultProfile</span></span>
<span data-ttu-id="19115-148">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="19115-148">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19115-149">-Описание</span><span class="sxs-lookup"><span data-stu-id="19115-149">-Description</span></span>
<span data-ttu-id="19115-150">Описание назначения политики</span><span class="sxs-lookup"><span data-stu-id="19115-150">The description for policy assignment</span></span>

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

### <span data-ttu-id="19115-151">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="19115-151">-DisplayName</span></span>
<span data-ttu-id="19115-152">Задает новое отображаемое имя для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="19115-152">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="19115-153">-EnforcementMode</span><span class="sxs-lookup"><span data-stu-id="19115-153">-EnforcementMode</span></span>
<span data-ttu-id="19115-154">Режим принудительного применения для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="19115-154">The enforcement mode for policy assignment.</span></span> <span data-ttu-id="19115-155">В настоящее время допустимые значения: Default. DoNotEnforce.</span><span class="sxs-lookup"><span data-stu-id="19115-155">Currently, valid values are Default, DoNotEnforce.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Policy.PolicyAssignmentEnforcementMode]
Parameter Sets: (All)
Aliases:
Accepted values: Default, DoNotEnforce

Required: False
Position: Named
Default value: Default
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19115-156">-ID</span><span class="sxs-lookup"><span data-stu-id="19115-156">-Id</span></span>
<span data-ttu-id="19115-157">Указывает полный идентификатор ресурса для назначения политики, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="19115-157">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet, PolicyParameterIdObjectParameterSet, PolicyParameterIdStringParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19115-158">-Location</span><span class="sxs-lookup"><span data-stu-id="19115-158">-Location</span></span>
<span data-ttu-id="19115-159">Расположение удостоверения ресурса для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="19115-159">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="19115-160">Это необходимо, если используется параметр-AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="19115-160">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="19115-161">-Metadata</span><span class="sxs-lookup"><span data-stu-id="19115-161">-Metadata</span></span>
<span data-ttu-id="19115-162">Обновленные метаданные для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="19115-162">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="19115-163">Это может быть либо путь к имени файла, содержащему метаданные, либо метаданные в виде строки.</span><span class="sxs-lookup"><span data-stu-id="19115-163">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="19115-164">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="19115-164">-Name</span></span>
<span data-ttu-id="19115-165">Указывает имя назначения политики, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="19115-165">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, PolicyParameterNameObjectParameterSet, PolicyParameterNameStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19115-166">-NotScope</span><span class="sxs-lookup"><span data-stu-id="19115-166">-NotScope</span></span>
<span data-ttu-id="19115-167">Назначение политики не является областью действия.</span><span class="sxs-lookup"><span data-stu-id="19115-167">The policy assignment not scopes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19115-168">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="19115-168">-PolicyParameter</span></span>
<span data-ttu-id="19115-169">Новый путь к файлу параметров политики или строковое значение для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="19115-169">The new policy parameters file path or string for the policy assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyParameterNameStringParameterSet, PolicyParameterIdStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19115-170">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="19115-170">-PolicyParameterObject</span></span>
<span data-ttu-id="19115-171">Новый объект параметров политики для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="19115-171">The new policy parameters object for the policy assignment.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: PolicyParameterNameObjectParameterSet, PolicyParameterIdObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19115-172">-Pre</span><span class="sxs-lookup"><span data-stu-id="19115-172">-Pre</span></span>
<span data-ttu-id="19115-173">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="19115-173">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="19115-174">-Scope</span><span class="sxs-lookup"><span data-stu-id="19115-174">-Scope</span></span>
<span data-ttu-id="19115-175">Указывает область применения политики.</span><span class="sxs-lookup"><span data-stu-id="19115-175">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, PolicyParameterNameObjectParameterSet, PolicyParameterNameStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19115-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19115-176">CommonParameters</span></span>
<span data-ttu-id="19115-177">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="19115-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19115-178">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="19115-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19115-179">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="19115-179">INPUTS</span></span>

### <span data-ttu-id="19115-180">System. String</span><span class="sxs-lookup"><span data-stu-id="19115-180">System.String</span></span>

### <span data-ttu-id="19115-181">System. String []</span><span class="sxs-lookup"><span data-stu-id="19115-181">System.String[]</span></span>

## <span data-ttu-id="19115-182">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="19115-182">OUTPUTS</span></span>

### <span data-ttu-id="19115-183">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="19115-183">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="19115-184">Пуск</span><span class="sxs-lookup"><span data-stu-id="19115-184">NOTES</span></span>

## <span data-ttu-id="19115-185">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="19115-185">RELATED LINKS</span></span>

[<span data-ttu-id="19115-186">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="19115-186">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="19115-187">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="19115-187">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="19115-188">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="19115-188">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)


