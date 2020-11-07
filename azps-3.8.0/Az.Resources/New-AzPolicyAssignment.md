---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
ms.openlocfilehash: 2ae25ea7679655c4bc10f8eea714cba851bc8c9c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912552"
---
# <span data-ttu-id="36fcc-101">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="36fcc-101">New-AzPolicyAssignment</span></span>

## <span data-ttu-id="36fcc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="36fcc-102">SYNOPSIS</span></span>
<span data-ttu-id="36fcc-103">Создание назначения политики.</span><span class="sxs-lookup"><span data-stu-id="36fcc-103">Creates a policy assignment.</span></span>

## <span data-ttu-id="36fcc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="36fcc-104">SYNTAX</span></span>

### <span data-ttu-id="36fcc-105">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="36fcc-105">DefaultParameterSet (Default)</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Metadata <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36fcc-106">PolicyParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="36fcc-106">PolicyParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36fcc-107">PolicyParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="36fcc-107">PolicyParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36fcc-108">PolicySetParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="36fcc-108">PolicySetParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36fcc-109">PolicySetParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="36fcc-109">PolicySetParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36fcc-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="36fcc-110">DESCRIPTION</span></span>
<span data-ttu-id="36fcc-111">Командлет **New-AzPolicyAssignment** создает назначение политики.</span><span class="sxs-lookup"><span data-stu-id="36fcc-111">The **New-AzPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="36fcc-112">Укажите политику и область действия.</span><span class="sxs-lookup"><span data-stu-id="36fcc-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="36fcc-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="36fcc-113">EXAMPLES</span></span>

### <span data-ttu-id="36fcc-114">Пример 1: назначение политики на уровне подписки</span><span class="sxs-lookup"><span data-stu-id="36fcc-114">Example 1: Policy assignment at subscription level</span></span>
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)"
```

<span data-ttu-id="36fcc-115">Первая команда получает подписку с именем Subscription01 с помощью командлета Get-AzSubscription и сохраняет его в переменной $Subscription.</span><span class="sxs-lookup"><span data-stu-id="36fcc-115">The first command gets a subscription named Subscription01 by using the Get-AzSubscription cmdlet and stores it in the $Subscription variable.</span></span>
<span data-ttu-id="36fcc-116">Вторая команда получает определение политики с именем VirtualMachinePolicy с помощью командлета Get-AzPolicyDefinition и сохраняет его в переменной $Policy.</span><span class="sxs-lookup"><span data-stu-id="36fcc-116">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="36fcc-117">Последняя команда назначает политику в $Policy на уровне подписки, определяемой строкой области действия подписки.</span><span class="sxs-lookup"><span data-stu-id="36fcc-117">The final command assigns the policy in $Policy at the level of the subscription identified by the subscription scope string.</span></span>

### <span data-ttu-id="36fcc-118">Пример 2: назначение политики на уровне группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="36fcc-118">Example 2: Policy assignment at resource group level</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="36fcc-119">Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью командлета Get-AzResourceGroup и сохраняет его в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="36fcc-119">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="36fcc-120">Вторая команда получает определение политики с именем VirtualMachinePolicy с помощью командлета Get-AzPolicyDefinition и сохраняет его в переменной $Policy.</span><span class="sxs-lookup"><span data-stu-id="36fcc-120">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="36fcc-121">Последняя команда назначает политику в $Policy на уровне группы ресурсов, определяемой свойством **ResourceId** $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="36fcc-121">The final command assigns the policy in $Policy at the level of the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="36fcc-122">Пример 3: назначение политики на уровне группы ресурсов с объектом параметра политики</span><span class="sxs-lookup"><span data-stu-id="36fcc-122">Example 3: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> $Locations = Get-AzLocation | where displayname -like '*east*'
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="36fcc-123">Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью командлета Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="36fcc-123">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="36fcc-124">Команда сохраняет этот объект в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="36fcc-124">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="36fcc-125">Вторая команда получает встроенное определение политики для допустимых местоположений с помощью командлета Get-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="36fcc-125">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="36fcc-126">Команда сохраняет этот объект в переменной $Policy.</span><span class="sxs-lookup"><span data-stu-id="36fcc-126">The command stores that object in the $Policy variable.</span></span>
<span data-ttu-id="36fcc-127">Третья и четвертая команды создают объект, содержащий все регионы Azure с именем "Восток".</span><span class="sxs-lookup"><span data-stu-id="36fcc-127">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="36fcc-128">Команды хранят этот объект в переменной $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="36fcc-128">The commands store that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="36fcc-129">Последняя команда назначает политику в $Policy на уровне группы ресурсов, используя объект параметра политики в $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="36fcc-129">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="36fcc-130">Свойство **ResourceId** для $ResourceGroup определяет группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="36fcc-130">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="36fcc-131">Пример 4: назначение политики на уровне группы ресурсов с помощью файла параметров политики</span><span class="sxs-lookup"><span data-stu-id="36fcc-131">Example 4: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="36fcc-132">Создайте файл с именем _AllowedLocations.js_ в локальном рабочем каталоге со следующим содержимым.</span><span class="sxs-lookup"><span data-stu-id="36fcc-132">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="36fcc-133">Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью командлета Get-AzResourceGroup и сохраняет его в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="36fcc-133">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="36fcc-134">Вторая команда получает встроенное определение политики для допустимых местоположений с помощью командлета Get-AzPolicyDefinition и сохраняет его в переменной $Policy.</span><span class="sxs-lookup"><span data-stu-id="36fcc-134">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="36fcc-135">Последняя команда назначает политику в $Policy в группе ресурсов, определяемой свойством **ResourceId** $ResourceGroup с помощью файла параметров политики AllowedLocations.json из локального рабочего каталога.</span><span class="sxs-lookup"><span data-stu-id="36fcc-135">The final command assigns the policy in $Policy at the resource group identified by the **ResourceId** property of $ResourceGroup using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="36fcc-136">Пример 5: назначение политики с управляемым удостоверением</span><span class="sxs-lookup"><span data-stu-id="36fcc-136">Example 5: Policy assignment with a managed identity</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -Location 'eastus' -AssignIdentity
```

<span data-ttu-id="36fcc-137">Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью командлета Get-AzResourceGroup и сохраняет его в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="36fcc-137">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="36fcc-138">Вторая команда получает определение политики с именем VirtualMachinePolicy с помощью командлета Get-AzPolicyDefinition и сохраняет его в переменной $Policy.</span><span class="sxs-lookup"><span data-stu-id="36fcc-138">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="36fcc-139">Последняя команда назначает политику в $Policy группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="36fcc-139">The final command assigns the policy in $Policy to the resource group.</span></span> <span data-ttu-id="36fcc-140">Управляемое удостоверение создается автоматически и назначается назначению политики.</span><span class="sxs-lookup"><span data-stu-id="36fcc-140">A managed identity is automatically created and assigned to the policy assignment.</span></span>

### <span data-ttu-id="36fcc-141">Пример 6: назначение политики с помощью свойства режима принудительного применения</span><span class="sxs-lookup"><span data-stu-id="36fcc-141">Example 6: Policy assignment with an enforcement mode property</span></span>
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)" -EnforcementMode DoNotEnforce
```

<span data-ttu-id="36fcc-142">Первая команда получает подписку с именем Subscription01 с помощью командлета Get-AzSubscription и сохраняет его в переменной $Subscription.</span><span class="sxs-lookup"><span data-stu-id="36fcc-142">The first command gets a subscription named Subscription01 by using the Get-AzSubscription cmdlet and stores it in the $Subscription variable.</span></span>
<span data-ttu-id="36fcc-143">Вторая команда получает определение политики с именем VirtualMachinePolicy с помощью командлета Get-AzPolicyDefinition и сохраняет его в переменной $Policy.</span><span class="sxs-lookup"><span data-stu-id="36fcc-143">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="36fcc-144">Последняя команда назначает политику в $Policy на уровне подписки, определяемой строкой области действия подписки.</span><span class="sxs-lookup"><span data-stu-id="36fcc-144">The final command assigns the policy in $Policy at the level of the subscription identified by the subscription scope string.</span></span> <span data-ttu-id="36fcc-145">Для задания задано значение EnforcementMode, равное _DoNotEnforce_ , т. е. эффект политики не применяется при создании или обновлении ресурсов.</span><span class="sxs-lookup"><span data-stu-id="36fcc-145">The assignment is set with an EnforcementMode value of _DoNotEnforce_ i.e. the policy effect is not enforced during resource creation or update.</span></span>

## <span data-ttu-id="36fcc-146">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="36fcc-146">PARAMETERS</span></span>

### <span data-ttu-id="36fcc-147">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="36fcc-147">-ApiVersion</span></span>
<span data-ttu-id="36fcc-148">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="36fcc-148">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="36fcc-149">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="36fcc-149">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="36fcc-150">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="36fcc-150">-AssignIdentity</span></span>
<span data-ttu-id="36fcc-151">Создание и назначение удостоверения Azure Active Directory для этого назначения политики.</span><span class="sxs-lookup"><span data-stu-id="36fcc-151">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="36fcc-152">Удостоверение будет использоваться при выполнении развертываний для политик "deployIfNotExists".</span><span class="sxs-lookup"><span data-stu-id="36fcc-152">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="36fcc-153">При назначении удостоверения требуется указать расположение.</span><span class="sxs-lookup"><span data-stu-id="36fcc-153">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="36fcc-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36fcc-154">-DefaultProfile</span></span>
<span data-ttu-id="36fcc-155">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="36fcc-155">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36fcc-156">-Описание</span><span class="sxs-lookup"><span data-stu-id="36fcc-156">-Description</span></span>
<span data-ttu-id="36fcc-157">Описание назначения политики</span><span class="sxs-lookup"><span data-stu-id="36fcc-157">The description for policy assignment</span></span>

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

### <span data-ttu-id="36fcc-158">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="36fcc-158">-DisplayName</span></span>
<span data-ttu-id="36fcc-159">Задает отображаемое имя для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="36fcc-159">Specifies a display name for the policy assignment.</span></span>

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

### <span data-ttu-id="36fcc-160">-EnforcementMode</span><span class="sxs-lookup"><span data-stu-id="36fcc-160">-EnforcementMode</span></span>
<span data-ttu-id="36fcc-161">Режим принудительного применения для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="36fcc-161">The enforcement mode for policy assignment.</span></span> <span data-ttu-id="36fcc-162">В настоящее время допустимые значения: Default. DoNotEnforce.</span><span class="sxs-lookup"><span data-stu-id="36fcc-162">Currently, valid values are Default, DoNotEnforce.</span></span>

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

### <span data-ttu-id="36fcc-163">-Location</span><span class="sxs-lookup"><span data-stu-id="36fcc-163">-Location</span></span>
<span data-ttu-id="36fcc-164">Расположение удостоверения ресурса для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="36fcc-164">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="36fcc-165">Это необходимо, если используется параметр-AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="36fcc-165">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="36fcc-166">-Metadata</span><span class="sxs-lookup"><span data-stu-id="36fcc-166">-Metadata</span></span>
<span data-ttu-id="36fcc-167">Метаданные для нового назначения политики.</span><span class="sxs-lookup"><span data-stu-id="36fcc-167">The metadata for the new policy assignment.</span></span> <span data-ttu-id="36fcc-168">Это может быть либо путь к имени файла, содержащему метаданные, либо метаданные в виде строки.</span><span class="sxs-lookup"><span data-stu-id="36fcc-168">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="36fcc-169">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="36fcc-169">-Name</span></span>
<span data-ttu-id="36fcc-170">Задает имя для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="36fcc-170">Specifies a name for the policy assignment.</span></span>

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

### <span data-ttu-id="36fcc-171">-NotScope</span><span class="sxs-lookup"><span data-stu-id="36fcc-171">-NotScope</span></span>
<span data-ttu-id="36fcc-172">Область "не для назначения политики".</span><span class="sxs-lookup"><span data-stu-id="36fcc-172">The not scopes for policy assignment.</span></span>

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

### <span data-ttu-id="36fcc-173">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="36fcc-173">-PolicyDefinition</span></span>
<span data-ttu-id="36fcc-174">Указывает политику как объект **PsPolicyDefinition** , который содержит правило политики.</span><span class="sxs-lookup"><span data-stu-id="36fcc-174">Specifies a policy, as a **PsPolicyDefinition** object that contains the policy rule.</span></span>

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

### <span data-ttu-id="36fcc-175">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="36fcc-175">-PolicyParameter</span></span>
<span data-ttu-id="36fcc-176">Путь к файлу параметра политики или строка параметра политики.</span><span class="sxs-lookup"><span data-stu-id="36fcc-176">The policy parameter file path or policy parameter string.</span></span>

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

### <span data-ttu-id="36fcc-177">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="36fcc-177">-PolicyParameterObject</span></span>
<span data-ttu-id="36fcc-178">Объект параметра политики.</span><span class="sxs-lookup"><span data-stu-id="36fcc-178">The policy parameter object.</span></span>

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

### <span data-ttu-id="36fcc-179">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="36fcc-179">-PolicySetDefinition</span></span>
<span data-ttu-id="36fcc-180">Объект определения параметра политики.</span><span class="sxs-lookup"><span data-stu-id="36fcc-180">The policy set definition object.</span></span>

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

### <span data-ttu-id="36fcc-181">-Pre</span><span class="sxs-lookup"><span data-stu-id="36fcc-181">-Pre</span></span>
<span data-ttu-id="36fcc-182">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="36fcc-182">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="36fcc-183">-Scope</span><span class="sxs-lookup"><span data-stu-id="36fcc-183">-Scope</span></span>
<span data-ttu-id="36fcc-184">Указывает область, в которой нужно назначить политику.</span><span class="sxs-lookup"><span data-stu-id="36fcc-184">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="36fcc-185">Например, чтобы назначить политику группе ресурсов, укажите следующее: `/subscriptions/` `/resourcegroups/` имя группы ресурсов для идентификатора подписки</span><span class="sxs-lookup"><span data-stu-id="36fcc-185">For instance, to assign a policy to a resource group, specify the following: `/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

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

### <span data-ttu-id="36fcc-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36fcc-186">CommonParameters</span></span>
<span data-ttu-id="36fcc-187">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="36fcc-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36fcc-188">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36fcc-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36fcc-189">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="36fcc-189">INPUTS</span></span>

### <span data-ttu-id="36fcc-190">System. String</span><span class="sxs-lookup"><span data-stu-id="36fcc-190">System.String</span></span>

### <span data-ttu-id="36fcc-191">System. String []</span><span class="sxs-lookup"><span data-stu-id="36fcc-191">System.String[]</span></span>

### <span data-ttu-id="36fcc-192">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="36fcc-192">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="36fcc-193">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="36fcc-193">OUTPUTS</span></span>

### <span data-ttu-id="36fcc-194">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="36fcc-194">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="36fcc-195">Пуск</span><span class="sxs-lookup"><span data-stu-id="36fcc-195">NOTES</span></span>

## <span data-ttu-id="36fcc-196">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="36fcc-196">RELATED LINKS</span></span>

[<span data-ttu-id="36fcc-197">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="36fcc-197">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="36fcc-198">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="36fcc-198">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="36fcc-199">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="36fcc-199">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="36fcc-200">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="36fcc-200">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


