---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
ms.openlocfilehash: 8efda1a15546a09f0946506f3bc7fd27462b3c03
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100235884"
---
# <span data-ttu-id="2c3f5-101">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="2c3f5-101">Set-AzPolicyAssignment</span></span>

## <span data-ttu-id="2c3f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c3f5-102">SYNOPSIS</span></span>
<span data-ttu-id="2c3f5-103">Изменяет назначение политики.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-103">Modifies a policy assignment.</span></span>

## <span data-ttu-id="2c3f5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2c3f5-104">SYNTAX</span></span>

### <span data-ttu-id="2c3f5-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2c3f5-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c3f5-106">PolicyParameterNameObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c3f5-106">PolicyParameterNameObjectParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity]
 [-Location <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c3f5-107">PolicyParameterNameStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c3f5-107">PolicyParameterNameStringParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c3f5-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c3f5-108">IdParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c3f5-109">PolicyParameterIdObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c3f5-109">PolicyParameterIdObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c3f5-110">PolicyParameterIdStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c3f5-110">PolicyParameterIdStringParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c3f5-111">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c3f5-111">InputObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] -InputObject <PsPolicyAssignment> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c3f5-112">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c3f5-112">DESCRIPTION</span></span>
<span data-ttu-id="2c3f5-113">**Cmdlet Set-AzPolicyAssignment** изменяет назначение политики.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-113">The **Set-AzPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="2c3f5-114">Укажите назначение по ИД или по имени и области.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-114">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="2c3f5-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2c3f5-115">EXAMPLES</span></span>

### <span data-ttu-id="2c3f5-116">Пример 1. Обновление отображаемом имени</span><span class="sxs-lookup"><span data-stu-id="2c3f5-116">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="2c3f5-117">Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью Get-AzResourceGroup командлета.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-117">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="2c3f5-118">Эта команда сохраняет этот объект в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-118">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="2c3f5-119">Вторая команда получает назначение политики PolicyAssignment с помощью Get-AzPolicyAssignment командлета.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-119">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="2c3f5-120">Эта команда сохраняет объект в переменной $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-120">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="2c3f5-121">Конечная команда обновляет отображаемую имя назначения политики для группы ресурсов, заданной свойством **ResourceId** $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-121">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="2c3f5-122">Пример 2. Добавление управляемого удостоверения в назначение политики</span><span class="sxs-lookup"><span data-stu-id="2c3f5-122">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="2c3f5-123">Первая команда получает назначение политики PolicyAssignment из текущей подписки с помощью Get-AzPolicyAssignment командлета.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-123">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="2c3f5-124">Эта команда сохраняет объект в переменной $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-124">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="2c3f5-125">Конечная команда назначает управляемое удостоверение назначению политики.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-125">The final command assigns a managed identity to the policy assignment.</span></span>

### <span data-ttu-id="2c3f5-126">Пример 3. Обновление параметров назначения политики с помощью нового объекта параметров политики</span><span class="sxs-lookup"><span data-stu-id="2c3f5-126">Example 3: Update policy assignment parameters with new policy parameter object</span></span>
```
PS C:\> $Locations = Get-AzLocation | where {($_.displayname -like 'france*') -or ($_.displayname -like 'uk*')}
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="2c3f5-127">Первая и вторая команды создают объект, содержащий все регионы Azure, имена которых начинаются со слова france или uk.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-127">The first and second commands create an object containing all Azure regions whose names start with "france" or "uk".</span></span>
<span data-ttu-id="2c3f5-128">Вторая команда сохраняет этот объект в переменной $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-128">The second command stores that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="2c3f5-129">Третья команда получает назначение политики "PolicyAssignment" и сохраняет объект в переменной $PolicyAssignment политика.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-129">The third command gets the policy assignment named 'PolicyAssignment' The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="2c3f5-130">Конечная команда обновляет значения параметров для назначения политики PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-130">The final command updates the parameter values on the policy assignment named PolicyAssignment.</span></span>

### <span data-ttu-id="2c3f5-131">Пример 4. Обновление параметров назначения политики с помощью файла параметров политики</span><span class="sxs-lookup"><span data-stu-id="2c3f5-131">Example 4: Update policy assignment parameters with policy parameter file</span></span>
<span data-ttu-id="2c3f5-132">Создайте файл сAllowedLocations.js _в_ локальном рабочем каталоге со следующим содержимым:</span><span class="sxs-lookup"><span data-stu-id="2c3f5-132">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="2c3f5-133">Команда обновляет назначение политики "PolicyAssignment", используя файл параметров политики, AllowedLocations.jsиз локального рабочего каталога.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-133">The command updates the policy assignment named 'PolicyAssignment' using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="2c3f5-134">Пример 5. Обновление режимов принудительных режимов</span><span class="sxs-lookup"><span data-stu-id="2c3f5-134">Example 5: Update an enforcementMode</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -EnforcementMode Default
```

<span data-ttu-id="2c3f5-135">Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью Get-AzResourceGroup командлета.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-135">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="2c3f5-136">Эта команда сохраняет этот объект в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-136">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="2c3f5-137">Вторая команда получает назначение политики PolicyAssignment с помощью Get-AzPolicyAssignment командлета.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-137">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="2c3f5-138">Эта команда сохраняет объект в переменной $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-138">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="2c3f5-139">Конечная команда обновляет свойство enforcementMode назначения политики для группы ресурсов, заданной свойством **ResourceId** $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-139">The final command updates the enforcementMode property on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

## <span data-ttu-id="2c3f5-140">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c3f5-140">PARAMETERS</span></span>

### <span data-ttu-id="2c3f5-141">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2c3f5-141">-ApiVersion</span></span>
<span data-ttu-id="2c3f5-142">Определяет версию API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-142">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="2c3f5-143">Если не указать версию, этот cmdlet использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-143">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="2c3f5-144">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="2c3f5-144">-AssignIdentity</span></span>
<span data-ttu-id="2c3f5-145">Создать и назначить удостоверение Azure Active Directory для этого назначения политики.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-145">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="2c3f5-146">Удостоверение будет использоваться при развертывании политик deployIfNotExists.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-146">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="2c3f5-147">Расположение требуется при назначении удостоверения.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-147">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="2c3f5-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c3f5-148">-DefaultProfile</span></span>
<span data-ttu-id="2c3f5-149">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2c3f5-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c3f5-150">-Description</span><span class="sxs-lookup"><span data-stu-id="2c3f5-150">-Description</span></span>
<span data-ttu-id="2c3f5-151">Описание назначения политики</span><span class="sxs-lookup"><span data-stu-id="2c3f5-151">The description for policy assignment</span></span>

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

### <span data-ttu-id="2c3f5-152">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2c3f5-152">-DisplayName</span></span>
<span data-ttu-id="2c3f5-153">Указывает новое отображаемого имя для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-153">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="2c3f5-154">-EnforcementMode</span><span class="sxs-lookup"><span data-stu-id="2c3f5-154">-EnforcementMode</span></span>
<span data-ttu-id="2c3f5-155">Режим обеспечения соблюдения при назначении политики.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-155">The enforcement mode for policy assignment.</span></span> <span data-ttu-id="2c3f5-156">В настоящее время допустимые значения: Default и DoNotEnforce.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-156">Currently, valid values are Default, DoNotEnforce.</span></span>

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

### <span data-ttu-id="2c3f5-157">-Id</span><span class="sxs-lookup"><span data-stu-id="2c3f5-157">-Id</span></span>
<span data-ttu-id="2c3f5-158">Указывает полностью определенный код ресурса для назначения политики, которую изменяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-158">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="2c3f5-159">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c3f5-159">-InputObject</span></span>
<span data-ttu-id="2c3f5-160">Объект назначения политики для обновления результатов из другого cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-160">The policy assignment object to update that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyAssignment
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c3f5-161">-Location</span><span class="sxs-lookup"><span data-stu-id="2c3f5-161">-Location</span></span>
<span data-ttu-id="2c3f5-162">Расположение идентификатора ресурса назначения политики.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-162">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="2c3f5-163">Это необходимо для использования переключателя -AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-163">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="2c3f5-164">-Метаданные</span><span class="sxs-lookup"><span data-stu-id="2c3f5-164">-Metadata</span></span>
<span data-ttu-id="2c3f5-165">Обновленные метаданные для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-165">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="2c3f5-166">Это может быть путь к имени файла, содержащего метаданные, или метаданные в виде строки.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-166">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="2c3f5-167">-Name</span><span class="sxs-lookup"><span data-stu-id="2c3f5-167">-Name</span></span>
<span data-ttu-id="2c3f5-168">Указывает имя назначения политики, которое изменяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-168">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="2c3f5-169">-NotScope</span><span class="sxs-lookup"><span data-stu-id="2c3f5-169">-NotScope</span></span>
<span data-ttu-id="2c3f5-170">Назначение политики не имеет областей.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-170">The policy assignment not scopes.</span></span>

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

### <span data-ttu-id="2c3f5-171">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="2c3f5-171">-PolicyParameter</span></span>
<span data-ttu-id="2c3f5-172">Путь или строка для назначения политики с параметрами новой политики.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-172">The new policy parameters file path or string for the policy assignment.</span></span>

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

### <span data-ttu-id="2c3f5-173">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="2c3f5-173">-PolicyParameterObject</span></span>
<span data-ttu-id="2c3f5-174">Объект параметров новой политики для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-174">The new policy parameters object for the policy assignment.</span></span>

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

### <span data-ttu-id="2c3f5-175">-Pre</span><span class="sxs-lookup"><span data-stu-id="2c3f5-175">-Pre</span></span>
<span data-ttu-id="2c3f5-176">Указывает на то, что этот cmdlet рассматривает предварительные версии API при автоматическом определении используемой версии.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-176">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="2c3f5-177">-Scope</span><span class="sxs-lookup"><span data-stu-id="2c3f5-177">-Scope</span></span>
<span data-ttu-id="2c3f5-178">Определяет область применения политики.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-178">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="2c3f5-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c3f5-179">CommonParameters</span></span>
<span data-ttu-id="2c3f5-180">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c3f5-181">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2c3f5-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c3f5-182">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2c3f5-182">INPUTS</span></span>

### <span data-ttu-id="2c3f5-183">System.String</span><span class="sxs-lookup"><span data-stu-id="2c3f5-183">System.String</span></span>

### <span data-ttu-id="2c3f5-184">System.String[]</span><span class="sxs-lookup"><span data-stu-id="2c3f5-184">System.String[]</span></span>

## <span data-ttu-id="2c3f5-185">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2c3f5-185">OUTPUTS</span></span>

### <span data-ttu-id="2c3f5-186">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="2c3f5-186">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="2c3f5-187">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2c3f5-187">NOTES</span></span>

## <span data-ttu-id="2c3f5-188">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2c3f5-188">RELATED LINKS</span></span>

[<span data-ttu-id="2c3f5-189">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="2c3f5-189">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="2c3f5-190">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="2c3f5-190">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="2c3f5-191">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="2c3f5-191">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)


