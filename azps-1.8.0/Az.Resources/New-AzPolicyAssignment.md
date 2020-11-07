---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
ms.openlocfilehash: 1b88fa6ea7a44d17843b72da162eec374e2c861f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729389"
---
# <span data-ttu-id="d6753-101">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="d6753-101">New-AzPolicyAssignment</span></span>

## <span data-ttu-id="d6753-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d6753-102">SYNOPSIS</span></span>
<span data-ttu-id="d6753-103">Создание назначения политики.</span><span class="sxs-lookup"><span data-stu-id="d6753-103">Creates a policy assignment.</span></span>

## <span data-ttu-id="d6753-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d6753-104">SYNTAX</span></span>

### <span data-ttu-id="d6753-105">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d6753-105">DefaultParameterSet (Default)</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Metadata <String>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6753-106">PolicyParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6753-106">PolicyParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6753-107">PolicyParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6753-107">PolicyParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6753-108">PolicySetParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6753-108">PolicySetParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6753-109">PolicySetParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6753-109">PolicySetParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6753-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6753-110">DESCRIPTION</span></span>
<span data-ttu-id="d6753-111">Командлет **New-AzPolicyAssignment** создает назначение политики.</span><span class="sxs-lookup"><span data-stu-id="d6753-111">The **New-AzPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="d6753-112">Укажите политику и область действия.</span><span class="sxs-lookup"><span data-stu-id="d6753-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="d6753-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d6753-113">EXAMPLES</span></span>

### <span data-ttu-id="d6753-114">Пример 1: назначение политики на уровне группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="d6753-114">Example 1: Policy assignment at resource group level</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="d6753-115">Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью командлета Get-AzResourceGroup и сохраняет его в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d6753-115">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="d6753-116">Вторая команда получает определение политики с именем VirtualMachinePolicy с помощью командлета Get-AzPolicyDefinition и сохраняет его в переменной $Policy.</span><span class="sxs-lookup"><span data-stu-id="d6753-116">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="d6753-117">Последняя команда назначает политику в $Policy на уровне группы ресурсов, определяемой свойством **ResourceId** $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d6753-117">The final command assigns the policy in $Policy at the level of the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="d6753-118">Пример 2: назначение политики на уровне группы ресурсов с объектом параметра политики</span><span class="sxs-lookup"><span data-stu-id="d6753-118">Example 2: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> $Locations = Get-AzLocation | where displayname -like '*east*'
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="d6753-119">Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью командлета Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d6753-119">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="d6753-120">Команда сохраняет этот объект в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d6753-120">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="d6753-121">Вторая команда получает встроенное определение политики для допустимых местоположений с помощью командлета Get-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="d6753-121">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="d6753-122">Команда сохраняет этот объект в переменной $Policy.</span><span class="sxs-lookup"><span data-stu-id="d6753-122">The command stores that object in the $Policy variable.</span></span>
<span data-ttu-id="d6753-123">Третья и четвертая команды создают объект, содержащий все регионы Azure с именем "Восток".</span><span class="sxs-lookup"><span data-stu-id="d6753-123">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="d6753-124">Команды хранят этот объект в переменной $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="d6753-124">The commands store that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="d6753-125">Последняя команда назначает политику в $Policy на уровне группы ресурсов, используя объект параметра политики в $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="d6753-125">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="d6753-126">Свойство **ResourceId** для $ResourceGroup определяет группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d6753-126">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="d6753-127">Пример 3: назначение политики на уровне группы ресурсов с помощью файла параметров политики</span><span class="sxs-lookup"><span data-stu-id="d6753-127">Example 3: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="d6753-128">Создайте файл с именем _AllowedLocations.js_ в локальном рабочем каталоге со следующим содержимым.</span><span class="sxs-lookup"><span data-stu-id="d6753-128">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

```
{
    "listOfAllowedLocations":  {
      "value": [
        "westus",
        "westeurope",
        "japanwest"
      ]
    }
}
```

```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameter .\AllowedLocations.json
```

<span data-ttu-id="d6753-129">Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью командлета Get-AzResourceGroup и сохраняет его в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d6753-129">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="d6753-130">Вторая команда получает встроенное определение политики для допустимых местоположений с помощью командлета Get-AzPolicyDefinition и сохраняет его в переменной $Policy.</span><span class="sxs-lookup"><span data-stu-id="d6753-130">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="d6753-131">Последняя команда назначает политику в $Policy в группе ресурсов, определяемой свойством **ResourceId** $ResourceGroup с помощью файла параметров политики AllowedLocations.json из локального рабочего каталога.</span><span class="sxs-lookup"><span data-stu-id="d6753-131">The final command assigns the policy in $Policy at the resource group identified by the **ResourceId** property of $ResourceGroup using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="d6753-132">Пример 4: назначение политики с управляемым удостоверением</span><span class="sxs-lookup"><span data-stu-id="d6753-132">Example 4: Policy assignment with a managed identity</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -Location 'eastus' -AssignIdentity
```

<span data-ttu-id="d6753-133">Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью командлета Get-AzResourceGroup и сохраняет его в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d6753-133">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="d6753-134">Вторая команда получает определение политики с именем VirtualMachinePolicy с помощью командлета Get-AzPolicyDefinition и сохраняет его в переменной $Policy.</span><span class="sxs-lookup"><span data-stu-id="d6753-134">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="d6753-135">Последняя команда назначает политику в $Policy группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d6753-135">The final command assigns the policy in $Policy to the resource group.</span></span> <span data-ttu-id="d6753-136">Управляемое удостоверение создается автоматически и назначается назначению политики.</span><span class="sxs-lookup"><span data-stu-id="d6753-136">A managed identity is automatically created and assigned to the policy assignment.</span></span>

## <span data-ttu-id="d6753-137">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d6753-137">PARAMETERS</span></span>

### <span data-ttu-id="d6753-138">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d6753-138">-ApiVersion</span></span>
<span data-ttu-id="d6753-139">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d6753-139">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="d6753-140">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="d6753-140">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="d6753-141">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="d6753-141">-AssignIdentity</span></span>
<span data-ttu-id="d6753-142">Создание и назначение удостоверения Azure Active Directory для этого назначения политики.</span><span class="sxs-lookup"><span data-stu-id="d6753-142">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="d6753-143">Удостоверение будет использоваться при выполнении развертываний для политик "deployIfNotExists".</span><span class="sxs-lookup"><span data-stu-id="d6753-143">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="d6753-144">При назначении удостоверения требуется указать расположение.</span><span class="sxs-lookup"><span data-stu-id="d6753-144">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="d6753-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6753-145">-DefaultProfile</span></span>
<span data-ttu-id="d6753-146">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d6753-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d6753-147">-Описание</span><span class="sxs-lookup"><span data-stu-id="d6753-147">-Description</span></span>
<span data-ttu-id="d6753-148">Описание назначения политики</span><span class="sxs-lookup"><span data-stu-id="d6753-148">The description for policy assignment</span></span>

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

### <span data-ttu-id="d6753-149">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d6753-149">-DisplayName</span></span>
<span data-ttu-id="d6753-150">Задает отображаемое имя для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="d6753-150">Specifies a display name for the policy assignment.</span></span>

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

### <span data-ttu-id="d6753-151">-Location</span><span class="sxs-lookup"><span data-stu-id="d6753-151">-Location</span></span>
<span data-ttu-id="d6753-152">Расположение удостоверения ресурса для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="d6753-152">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="d6753-153">Это необходимо, если используется параметр-AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="d6753-153">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="d6753-154">-Metadata</span><span class="sxs-lookup"><span data-stu-id="d6753-154">-Metadata</span></span>
<span data-ttu-id="d6753-155">Метаданные для нового назначения политики.</span><span class="sxs-lookup"><span data-stu-id="d6753-155">The metadata for the new policy assignment.</span></span> <span data-ttu-id="d6753-156">Это может быть либо путь к имени файла, содержащему метаданные, либо метаданные в виде строки.</span><span class="sxs-lookup"><span data-stu-id="d6753-156">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="d6753-157">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d6753-157">-Name</span></span>
<span data-ttu-id="d6753-158">Задает имя для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="d6753-158">Specifies a name for the policy assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6753-159">-NotScope</span><span class="sxs-lookup"><span data-stu-id="d6753-159">-NotScope</span></span>
<span data-ttu-id="d6753-160">Область "не для назначения политики".</span><span class="sxs-lookup"><span data-stu-id="d6753-160">The not scopes for policy assignment.</span></span>

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

### <span data-ttu-id="d6753-161">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d6753-161">-PolicyDefinition</span></span>
<span data-ttu-id="d6753-162">Указывает политику как объект **PsPolicyDefinition** , который содержит правило политики.</span><span class="sxs-lookup"><span data-stu-id="d6753-162">Specifies a policy, as a **PsPolicyDefinition** object that contains the policy rule.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicyParameterObjectParameterSet, PolicyParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicySetParameterObjectParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6753-163">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="d6753-163">-PolicyParameter</span></span>
<span data-ttu-id="d6753-164">Путь к файлу параметра политики или строка параметра политики.</span><span class="sxs-lookup"><span data-stu-id="d6753-164">The policy parameter file path or policy parameter string.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyParameterStringParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6753-165">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="d6753-165">-PolicyParameterObject</span></span>
<span data-ttu-id="d6753-166">Объект параметра политики.</span><span class="sxs-lookup"><span data-stu-id="d6753-166">The policy parameter object.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: PolicyParameterObjectParameterSet, PolicySetParameterObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6753-167">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="d6753-167">-PolicySetDefinition</span></span>
<span data-ttu-id="d6753-168">Объект определения параметра политики.</span><span class="sxs-lookup"><span data-stu-id="d6753-168">The policy set definition object.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicyParameterObjectParameterSet, PolicyParameterStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicySetParameterObjectParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6753-169">-Pre</span><span class="sxs-lookup"><span data-stu-id="d6753-169">-Pre</span></span>
<span data-ttu-id="d6753-170">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="d6753-170">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="d6753-171">-Scope</span><span class="sxs-lookup"><span data-stu-id="d6753-171">-Scope</span></span>
<span data-ttu-id="d6753-172">Указывает область, в которой нужно назначить политику.</span><span class="sxs-lookup"><span data-stu-id="d6753-172">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="d6753-173">Например, чтобы назначить политику группе ресурсов, укажите следующее: `/subscriptions/` `/resourcegroups/` имя группы ресурсов для идентификатора подписки</span><span class="sxs-lookup"><span data-stu-id="d6753-173">For instance, to assign a policy to a resource group, specify the following: `/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6753-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6753-174">CommonParameters</span></span>
<span data-ttu-id="d6753-175">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d6753-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6753-176">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6753-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6753-177">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d6753-177">INPUTS</span></span>

### <span data-ttu-id="d6753-178">System. String</span><span class="sxs-lookup"><span data-stu-id="d6753-178">System.String</span></span>

### <span data-ttu-id="d6753-179">System. String []</span><span class="sxs-lookup"><span data-stu-id="d6753-179">System.String[]</span></span>

### <span data-ttu-id="d6753-180">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="d6753-180">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="d6753-181">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6753-181">OUTPUTS</span></span>

### <span data-ttu-id="d6753-182">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="d6753-182">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="d6753-183">Пуск</span><span class="sxs-lookup"><span data-stu-id="d6753-183">NOTES</span></span>

## <span data-ttu-id="d6753-184">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d6753-184">RELATED LINKS</span></span>

[<span data-ttu-id="d6753-185">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d6753-185">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="d6753-186">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="d6753-186">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="d6753-187">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="d6753-187">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="d6753-188">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="d6753-188">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


