---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
ms.openlocfilehash: 63efc580cf47274363f04750dc6a3f8da93b6665
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235898"
---
# <span data-ttu-id="31754-101">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="31754-101">New-AzPolicyAssignment</span></span>

## <span data-ttu-id="31754-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="31754-102">SYNOPSIS</span></span>
<span data-ttu-id="31754-103">Создание назначения политики.</span><span class="sxs-lookup"><span data-stu-id="31754-103">Creates a policy assignment.</span></span>

## <span data-ttu-id="31754-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="31754-104">SYNTAX</span></span>

### <span data-ttu-id="31754-105">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="31754-105">DefaultParameterSet (Default)</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>]
 [-PolicySetDefinition <PsPolicySetDefinition>] [-Metadata <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31754-106">PolicyParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="31754-106">PolicyParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PsPolicyDefinition> [-PolicySetDefinition <PsPolicySetDefinition>]
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31754-107">PolicyParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="31754-107">PolicyParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PsPolicyDefinition> [-PolicySetDefinition <PsPolicySetDefinition>]
 -PolicyParameter <String> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31754-108">PolicySetParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="31754-108">PolicySetParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>] -PolicySetDefinition <PsPolicySetDefinition>
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31754-109">PolicySetParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="31754-109">PolicySetParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>] -PolicySetDefinition <PsPolicySetDefinition>
 -PolicyParameter <String> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31754-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="31754-110">DESCRIPTION</span></span>
<span data-ttu-id="31754-111">Командлет **New-AzPolicyAssignment** создает назначение политики.</span><span class="sxs-lookup"><span data-stu-id="31754-111">The **New-AzPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="31754-112">Укажите политику и область действия.</span><span class="sxs-lookup"><span data-stu-id="31754-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="31754-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="31754-113">EXAMPLES</span></span>

### <span data-ttu-id="31754-114">Пример 1: назначение политики на уровне подписки</span><span class="sxs-lookup"><span data-stu-id="31754-114">Example 1: Policy assignment at subscription level</span></span>
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)"
```

<span data-ttu-id="31754-115">Первая команда получает подписку с именем Subscription01 с помощью командлета Get-AzSubscription и сохраняет его в переменной $Subscription.</span><span class="sxs-lookup"><span data-stu-id="31754-115">The first command gets a subscription named Subscription01 by using the Get-AzSubscription cmdlet and stores it in the $Subscription variable.</span></span>
<span data-ttu-id="31754-116">Вторая команда получает определение политики с именем VirtualMachinePolicy с помощью командлета Get-AzPolicyDefinition и сохраняет его в переменной $Policy.</span><span class="sxs-lookup"><span data-stu-id="31754-116">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="31754-117">Последняя команда назначает политику в $Policy на уровне подписки, определяемой строкой области действия подписки.</span><span class="sxs-lookup"><span data-stu-id="31754-117">The final command assigns the policy in $Policy at the level of the subscription identified by the subscription scope string.</span></span>

### <span data-ttu-id="31754-118">Пример 2: назначение политики на уровне группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="31754-118">Example 2: Policy assignment at resource group level</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="31754-119">Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью командлета Get-AzResourceGroup и сохраняет его в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="31754-119">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="31754-120">Вторая команда получает определение политики с именем VirtualMachinePolicy с помощью командлета Get-AzPolicyDefinition и сохраняет его в переменной $Policy.</span><span class="sxs-lookup"><span data-stu-id="31754-120">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="31754-121">Последняя команда назначает политику в $Policy на уровне группы ресурсов, определяемой свойством **ResourceId** $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="31754-121">The final command assigns the policy in $Policy at the level of the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="31754-122">Пример 3: назначение политики на уровне группы ресурсов с объектом параметра политики</span><span class="sxs-lookup"><span data-stu-id="31754-122">Example 3: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> $Locations = Get-AzLocation | where displayname -like '*east*'
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="31754-123">Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью командлета Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="31754-123">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="31754-124">Команда сохраняет этот объект в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="31754-124">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="31754-125">Вторая команда получает встроенное определение политики для допустимых местоположений с помощью командлета Get-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="31754-125">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="31754-126">Команда сохраняет этот объект в переменной $Policy.</span><span class="sxs-lookup"><span data-stu-id="31754-126">The command stores that object in the $Policy variable.</span></span>
<span data-ttu-id="31754-127">Третья и четвертая команды создают объект, содержащий все регионы Azure с именем "Восток".</span><span class="sxs-lookup"><span data-stu-id="31754-127">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="31754-128">Команды хранят этот объект в переменной $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="31754-128">The commands store that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="31754-129">Последняя команда назначает политику в $Policy на уровне группы ресурсов, используя объект параметра политики в $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="31754-129">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="31754-130">Свойство **ResourceId** для $ResourceGroup определяет группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="31754-130">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="31754-131">Пример 4: назначение политики на уровне группы ресурсов с помощью файла параметров политики</span><span class="sxs-lookup"><span data-stu-id="31754-131">Example 4: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="31754-132">Создайте файл с именем _AllowedLocations.js_ в локальном рабочем каталоге со следующим содержимым.</span><span class="sxs-lookup"><span data-stu-id="31754-132">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="31754-133">Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью командлета Get-AzResourceGroup и сохраняет его в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="31754-133">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="31754-134">Вторая команда получает встроенное определение политики для допустимых местоположений с помощью командлета Get-AzPolicyDefinition и сохраняет его в переменной $Policy.</span><span class="sxs-lookup"><span data-stu-id="31754-134">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="31754-135">Последняя команда назначает политику в $Policy в группе ресурсов, определяемой свойством **ResourceId** $ResourceGroup с помощью файла параметров политики AllowedLocations.json из локального рабочего каталога.</span><span class="sxs-lookup"><span data-stu-id="31754-135">The final command assigns the policy in $Policy at the resource group identified by the **ResourceId** property of $ResourceGroup using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="31754-136">Пример 5: назначение политики с управляемым удостоверением</span><span class="sxs-lookup"><span data-stu-id="31754-136">Example 5: Policy assignment with a managed identity</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -Location 'eastus' -AssignIdentity
```

<span data-ttu-id="31754-137">Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью командлета Get-AzResourceGroup и сохраняет его в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="31754-137">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="31754-138">Вторая команда получает определение политики с именем VirtualMachinePolicy с помощью командлета Get-AzPolicyDefinition и сохраняет его в переменной $Policy.</span><span class="sxs-lookup"><span data-stu-id="31754-138">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="31754-139">Последняя команда назначает политику в $Policy группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="31754-139">The final command assigns the policy in $Policy to the resource group.</span></span> <span data-ttu-id="31754-140">Управляемое удостоверение создается автоматически и назначается назначению политики.</span><span class="sxs-lookup"><span data-stu-id="31754-140">A managed identity is automatically created and assigned to the policy assignment.</span></span>

### <span data-ttu-id="31754-141">Пример 6: назначение политики с помощью свойства режима принудительного применения</span><span class="sxs-lookup"><span data-stu-id="31754-141">Example 6: Policy assignment with an enforcement mode property</span></span>
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)" -EnforcementMode DoNotEnforce
```

<span data-ttu-id="31754-142">Первая команда получает подписку с именем Subscription01 с помощью командлета Get-AzSubscription и сохраняет его в переменной $Subscription.</span><span class="sxs-lookup"><span data-stu-id="31754-142">The first command gets a subscription named Subscription01 by using the Get-AzSubscription cmdlet and stores it in the $Subscription variable.</span></span>
<span data-ttu-id="31754-143">Вторая команда получает определение политики с именем VirtualMachinePolicy с помощью командлета Get-AzPolicyDefinition и сохраняет его в переменной $Policy.</span><span class="sxs-lookup"><span data-stu-id="31754-143">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="31754-144">Последняя команда назначает политику в $Policy на уровне подписки, определяемой строкой области действия подписки.</span><span class="sxs-lookup"><span data-stu-id="31754-144">The final command assigns the policy in $Policy at the level of the subscription identified by the subscription scope string.</span></span> <span data-ttu-id="31754-145">Для задания задано значение EnforcementMode, равное _DoNotEnforce_ , т. е. эффект политики не применяется при создании или обновлении ресурсов.</span><span class="sxs-lookup"><span data-stu-id="31754-145">The assignment is set with an EnforcementMode value of _DoNotEnforce_ i.e. the policy effect is not enforced during resource creation or update.</span></span>

## <span data-ttu-id="31754-146">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="31754-146">PARAMETERS</span></span>

### <span data-ttu-id="31754-147">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="31754-147">-ApiVersion</span></span>
<span data-ttu-id="31754-148">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="31754-148">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="31754-149">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="31754-149">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="31754-150">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="31754-150">-AssignIdentity</span></span>
<span data-ttu-id="31754-151">Создание и назначение удостоверения Azure Active Directory для этого назначения политики.</span><span class="sxs-lookup"><span data-stu-id="31754-151">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="31754-152">Удостоверение будет использоваться при выполнении развертываний для политик "deployIfNotExists".</span><span class="sxs-lookup"><span data-stu-id="31754-152">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="31754-153">При назначении удостоверения требуется указать расположение.</span><span class="sxs-lookup"><span data-stu-id="31754-153">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="31754-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31754-154">-DefaultProfile</span></span>
<span data-ttu-id="31754-155">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="31754-155">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="31754-156">-Описание</span><span class="sxs-lookup"><span data-stu-id="31754-156">-Description</span></span>
<span data-ttu-id="31754-157">Описание назначения политики</span><span class="sxs-lookup"><span data-stu-id="31754-157">The description for policy assignment</span></span>

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

### <span data-ttu-id="31754-158">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="31754-158">-DisplayName</span></span>
<span data-ttu-id="31754-159">Задает отображаемое имя для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="31754-159">Specifies a display name for the policy assignment.</span></span>

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

### <span data-ttu-id="31754-160">-EnforcementMode</span><span class="sxs-lookup"><span data-stu-id="31754-160">-EnforcementMode</span></span>
<span data-ttu-id="31754-161">Режим принудительного применения для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="31754-161">The enforcement mode for policy assignment.</span></span> <span data-ttu-id="31754-162">В настоящее время допустимые значения: Default. DoNotEnforce.</span><span class="sxs-lookup"><span data-stu-id="31754-162">Currently, valid values are Default, DoNotEnforce.</span></span>

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

### <span data-ttu-id="31754-163">-Location</span><span class="sxs-lookup"><span data-stu-id="31754-163">-Location</span></span>
<span data-ttu-id="31754-164">Расположение удостоверения ресурса для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="31754-164">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="31754-165">Это необходимо, если используется параметр-AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="31754-165">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="31754-166">-Metadata</span><span class="sxs-lookup"><span data-stu-id="31754-166">-Metadata</span></span>
<span data-ttu-id="31754-167">Метаданные для нового назначения политики.</span><span class="sxs-lookup"><span data-stu-id="31754-167">The metadata for the new policy assignment.</span></span> <span data-ttu-id="31754-168">Это может быть либо путь к имени файла, содержащему метаданные, либо метаданные в виде строки.</span><span class="sxs-lookup"><span data-stu-id="31754-168">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="31754-169">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="31754-169">-Name</span></span>
<span data-ttu-id="31754-170">Задает имя для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="31754-170">Specifies a name for the policy assignment.</span></span>

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

### <span data-ttu-id="31754-171">-NotScope</span><span class="sxs-lookup"><span data-stu-id="31754-171">-NotScope</span></span>
<span data-ttu-id="31754-172">Область "не для назначения политики".</span><span class="sxs-lookup"><span data-stu-id="31754-172">The not scopes for policy assignment.</span></span>

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

### <span data-ttu-id="31754-173">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="31754-173">-PolicyDefinition</span></span>
<span data-ttu-id="31754-174">Указывает политику как объект **PsPolicyDefinition** , который содержит правило политики.</span><span class="sxs-lookup"><span data-stu-id="31754-174">Specifies a policy, as a **PsPolicyDefinition** object that contains the policy rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyDefinition
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyDefinition
Parameter Sets: PolicyParameterObjectParameterSet, PolicyParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyDefinition
Parameter Sets: PolicySetParameterObjectParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31754-175">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="31754-175">-PolicyParameter</span></span>
<span data-ttu-id="31754-176">Путь к файлу параметра политики или строка параметра политики.</span><span class="sxs-lookup"><span data-stu-id="31754-176">The policy parameter file path or policy parameter string.</span></span>

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

### <span data-ttu-id="31754-177">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="31754-177">-PolicyParameterObject</span></span>
<span data-ttu-id="31754-178">Объект параметра политики.</span><span class="sxs-lookup"><span data-stu-id="31754-178">The policy parameter object.</span></span>

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

### <span data-ttu-id="31754-179">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="31754-179">-PolicySetDefinition</span></span>
<span data-ttu-id="31754-180">Объект определения параметра политики.</span><span class="sxs-lookup"><span data-stu-id="31754-180">The policy set definition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicySetDefinition
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicySetDefinition
Parameter Sets: PolicyParameterObjectParameterSet, PolicyParameterStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicySetDefinition
Parameter Sets: PolicySetParameterObjectParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31754-181">-Pre</span><span class="sxs-lookup"><span data-stu-id="31754-181">-Pre</span></span>
<span data-ttu-id="31754-182">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="31754-182">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="31754-183">-Scope</span><span class="sxs-lookup"><span data-stu-id="31754-183">-Scope</span></span>
<span data-ttu-id="31754-184">Указывает область, в которой нужно назначить политику.</span><span class="sxs-lookup"><span data-stu-id="31754-184">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="31754-185">Например, чтобы назначить политику группе ресурсов, укажите следующее: `/subscriptions/` `/resourcegroups/` имя группы ресурсов для идентификатора подписки</span><span class="sxs-lookup"><span data-stu-id="31754-185">For instance, to assign a policy to a resource group, specify the following: `/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

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

### <span data-ttu-id="31754-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31754-186">CommonParameters</span></span>
<span data-ttu-id="31754-187">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="31754-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31754-188">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="31754-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31754-189">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="31754-189">INPUTS</span></span>

### <span data-ttu-id="31754-190">System. String</span><span class="sxs-lookup"><span data-stu-id="31754-190">System.String</span></span>

### <span data-ttu-id="31754-191">System. String []</span><span class="sxs-lookup"><span data-stu-id="31754-191">System.String[]</span></span>

### <span data-ttu-id="31754-192">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="31754-192">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="31754-193">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="31754-193">OUTPUTS</span></span>

### <span data-ttu-id="31754-194">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="31754-194">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="31754-195">Пуск</span><span class="sxs-lookup"><span data-stu-id="31754-195">NOTES</span></span>

## <span data-ttu-id="31754-196">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="31754-196">RELATED LINKS</span></span>

[<span data-ttu-id="31754-197">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="31754-197">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="31754-198">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="31754-198">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="31754-199">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="31754-199">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="31754-200">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="31754-200">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


