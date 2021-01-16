---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
ms.openlocfilehash: 63efc580cf47274363f04750dc6a3f8da93b6665
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409628"
---
# <span data-ttu-id="7501c-101">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="7501c-101">New-AzPolicyAssignment</span></span>

## <span data-ttu-id="7501c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7501c-102">SYNOPSIS</span></span>
<span data-ttu-id="7501c-103">Создает назначение политики.</span><span class="sxs-lookup"><span data-stu-id="7501c-103">Creates a policy assignment.</span></span>

## <span data-ttu-id="7501c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7501c-104">SYNTAX</span></span>

### <span data-ttu-id="7501c-105">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7501c-105">DefaultParameterSet (Default)</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>]
 [-PolicySetDefinition <PsPolicySetDefinition>] [-Metadata <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7501c-106">PolicyParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7501c-106">PolicyParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PsPolicyDefinition> [-PolicySetDefinition <PsPolicySetDefinition>]
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7501c-107">PolicyParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="7501c-107">PolicyParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PsPolicyDefinition> [-PolicySetDefinition <PsPolicySetDefinition>]
 -PolicyParameter <String> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7501c-108">PolicySetParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7501c-108">PolicySetParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>] -PolicySetDefinition <PsPolicySetDefinition>
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7501c-109">PolicySetParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="7501c-109">PolicySetParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>] -PolicySetDefinition <PsPolicySetDefinition>
 -PolicyParameter <String> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7501c-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7501c-110">DESCRIPTION</span></span>
<span data-ttu-id="7501c-111">Для создания назначения политики будет создаваться **cmdlet New-AzPolicyAssignment.**</span><span class="sxs-lookup"><span data-stu-id="7501c-111">The **New-AzPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="7501c-112">Укажите политику и область действия.</span><span class="sxs-lookup"><span data-stu-id="7501c-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="7501c-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7501c-113">EXAMPLES</span></span>

### <span data-ttu-id="7501c-114">Пример 1. Назначение политики на уровне подписки</span><span class="sxs-lookup"><span data-stu-id="7501c-114">Example 1: Policy assignment at subscription level</span></span>
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)"
```

<span data-ttu-id="7501c-115">Первая команда получает подписку с именем Subscription01 с Get-AzSubscription командлетом и сохраняет ее в переменной $Subscription.</span><span class="sxs-lookup"><span data-stu-id="7501c-115">The first command gets a subscription named Subscription01 by using the Get-AzSubscription cmdlet and stores it in the $Subscription variable.</span></span>
<span data-ttu-id="7501c-116">Вторая команда получает определение политики VirtualMachinePolicy с помощью Get-AzPolicyDefinition и сохраняет его в переменной $Policy.</span><span class="sxs-lookup"><span data-stu-id="7501c-116">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="7501c-117">Конечная команда назначает политику в $Policy на уровне подписки, задаемой строкой области подписки.</span><span class="sxs-lookup"><span data-stu-id="7501c-117">The final command assigns the policy in $Policy at the level of the subscription identified by the subscription scope string.</span></span>

### <span data-ttu-id="7501c-118">Пример 2. Назначение политик на уровне группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="7501c-118">Example 2: Policy assignment at resource group level</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="7501c-119">Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью Get-AzResourceGroup и сохраняет ее в $ResourceGroup переменной.</span><span class="sxs-lookup"><span data-stu-id="7501c-119">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="7501c-120">Вторая команда получает определение политики VirtualMachinePolicy с помощью Get-AzPolicyDefinition и сохраняет его в переменной $Policy.</span><span class="sxs-lookup"><span data-stu-id="7501c-120">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="7501c-121">Конечная команда назначает политику в $Policy на уровне группы ресурсов, заданной свойством **ResourceId** $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7501c-121">The final command assigns the policy in $Policy at the level of the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="7501c-122">Пример 3. Назначение политики на уровне группы ресурсов с объектом-параметром политики</span><span class="sxs-lookup"><span data-stu-id="7501c-122">Example 3: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> $Locations = Get-AzLocation | where displayname -like '*east*'
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="7501c-123">Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью Get-AzResourceGroup командлета.</span><span class="sxs-lookup"><span data-stu-id="7501c-123">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="7501c-124">Эта команда сохраняет этот объект в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7501c-124">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="7501c-125">Вторая команда получает встроенное определение политики для разрешенных местоположений с помощью Get-AzPolicyDefinition командлета.</span><span class="sxs-lookup"><span data-stu-id="7501c-125">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="7501c-126">Эта команда сохраняет этот объект в $Policy переменной.</span><span class="sxs-lookup"><span data-stu-id="7501c-126">The command stores that object in the $Policy variable.</span></span>
<span data-ttu-id="7501c-127">Третья и четвертая команды создают объект, содержащий все регионы Azure с "востоком" в имени.</span><span class="sxs-lookup"><span data-stu-id="7501c-127">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="7501c-128">В командах этот объект хранится в переменной $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="7501c-128">The commands store that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="7501c-129">Конечная команда назначает политику в $Policy на уровне группы ресурсов с использованием объекта параметров политики в $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="7501c-129">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="7501c-130">Свойство **ResourceId** свойства $ResourceGroup определяет группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7501c-130">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="7501c-131">Пример 4. Назначение политики на уровне группы ресурсов с файлом параметров политики</span><span class="sxs-lookup"><span data-stu-id="7501c-131">Example 4: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="7501c-132">Создайте файл сAllowedLocations.js _в_ локальном рабочем каталоге со следующим содержимым:</span><span class="sxs-lookup"><span data-stu-id="7501c-132">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="7501c-133">Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью Get-AzResourceGroup и сохраняет ее в $ResourceGroup переменной.</span><span class="sxs-lookup"><span data-stu-id="7501c-133">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="7501c-134">Вторая команда получает встроенное определение политики для разрешенных местоположений с Get-AzPolicyDefinition и сохраняет его в переменной $Policy политики.</span><span class="sxs-lookup"><span data-stu-id="7501c-134">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="7501c-135">Конечная команда назначает политику в папке $Policy группе ресурсов, заданной свойством ResourceId свойства **$ResourceGroup,** используя файл параметров политики, AllowedLocations.jsиз локального рабочего каталога.</span><span class="sxs-lookup"><span data-stu-id="7501c-135">The final command assigns the policy in $Policy at the resource group identified by the **ResourceId** property of $ResourceGroup using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="7501c-136">Пример 5. Назначение политики с управляемым удостоверением</span><span class="sxs-lookup"><span data-stu-id="7501c-136">Example 5: Policy assignment with a managed identity</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -Location 'eastus' -AssignIdentity
```

<span data-ttu-id="7501c-137">Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью Get-AzResourceGroup и сохраняет ее в $ResourceGroup переменной.</span><span class="sxs-lookup"><span data-stu-id="7501c-137">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="7501c-138">Вторая команда получает определение политики VirtualMachinePolicy с помощью Get-AzPolicyDefinition и сохраняет его в переменной $Policy.</span><span class="sxs-lookup"><span data-stu-id="7501c-138">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="7501c-139">Конечная команда назначает политику в $Policy группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7501c-139">The final command assigns the policy in $Policy to the resource group.</span></span> <span data-ttu-id="7501c-140">Управляемое удостоверение будет создано автоматически и назначено назначению политики.</span><span class="sxs-lookup"><span data-stu-id="7501c-140">A managed identity is automatically created and assigned to the policy assignment.</span></span>

### <span data-ttu-id="7501c-141">Пример 6. Назначение политики со свойством режима принуителя</span><span class="sxs-lookup"><span data-stu-id="7501c-141">Example 6: Policy assignment with an enforcement mode property</span></span>
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)" -EnforcementMode DoNotEnforce
```

<span data-ttu-id="7501c-142">Первая команда получает подписку с именем Subscription01 с Get-AzSubscription командлетом и сохраняет ее в переменной $Subscription.</span><span class="sxs-lookup"><span data-stu-id="7501c-142">The first command gets a subscription named Subscription01 by using the Get-AzSubscription cmdlet and stores it in the $Subscription variable.</span></span>
<span data-ttu-id="7501c-143">Вторая команда получает определение политики VirtualMachinePolicy с помощью Get-AzPolicyDefinition и сохраняет его в переменной $Policy.</span><span class="sxs-lookup"><span data-stu-id="7501c-143">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="7501c-144">Конечная команда назначает политику в $Policy на уровне подписки, задаемой строкой области подписки.</span><span class="sxs-lookup"><span data-stu-id="7501c-144">The final command assigns the policy in $Policy at the level of the subscription identified by the subscription scope string.</span></span> <span data-ttu-id="7501c-145">Для назначения задано значение EnforcementMode _для DoNotEnforce,_ то есть действие политики не будет применяться при создании или обновлении ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7501c-145">The assignment is set with an EnforcementMode value of _DoNotEnforce_ i.e. the policy effect is not enforced during resource creation or update.</span></span>

## <span data-ttu-id="7501c-146">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7501c-146">PARAMETERS</span></span>

### <span data-ttu-id="7501c-147">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7501c-147">-ApiVersion</span></span>
<span data-ttu-id="7501c-148">Определяет версию API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7501c-148">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="7501c-149">Если не указать версию, этот cmdlet использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="7501c-149">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="7501c-150">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="7501c-150">-AssignIdentity</span></span>
<span data-ttu-id="7501c-151">Создание и назначение удостоверения Azure Active Directory для этого назначения политики.</span><span class="sxs-lookup"><span data-stu-id="7501c-151">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="7501c-152">Удостоверение будет использоваться при развертывании политик развертыванияIfNotExists.</span><span class="sxs-lookup"><span data-stu-id="7501c-152">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="7501c-153">При назначении удостоверения требуется расположение.</span><span class="sxs-lookup"><span data-stu-id="7501c-153">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="7501c-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7501c-154">-DefaultProfile</span></span>
<span data-ttu-id="7501c-155">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7501c-155">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7501c-156">-Description</span><span class="sxs-lookup"><span data-stu-id="7501c-156">-Description</span></span>
<span data-ttu-id="7501c-157">Описание назначения политики</span><span class="sxs-lookup"><span data-stu-id="7501c-157">The description for policy assignment</span></span>

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

### <span data-ttu-id="7501c-158">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7501c-158">-DisplayName</span></span>
<span data-ttu-id="7501c-159">Отображает имя для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="7501c-159">Specifies a display name for the policy assignment.</span></span>

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

### <span data-ttu-id="7501c-160">-EnforcementMode</span><span class="sxs-lookup"><span data-stu-id="7501c-160">-EnforcementMode</span></span>
<span data-ttu-id="7501c-161">Режим обеспечения безопасности при назначении политики.</span><span class="sxs-lookup"><span data-stu-id="7501c-161">The enforcement mode for policy assignment.</span></span> <span data-ttu-id="7501c-162">В настоящее время допустимые значения: Default и DoNotEnforce.</span><span class="sxs-lookup"><span data-stu-id="7501c-162">Currently, valid values are Default, DoNotEnforce.</span></span>

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

### <span data-ttu-id="7501c-163">-Location</span><span class="sxs-lookup"><span data-stu-id="7501c-163">-Location</span></span>
<span data-ttu-id="7501c-164">Расположение идентификатора ресурса назначения политики.</span><span class="sxs-lookup"><span data-stu-id="7501c-164">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="7501c-165">Это необходимо для использования переключателя -AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="7501c-165">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="7501c-166">-Метаданные</span><span class="sxs-lookup"><span data-stu-id="7501c-166">-Metadata</span></span>
<span data-ttu-id="7501c-167">Метаданные для нового назначения политики.</span><span class="sxs-lookup"><span data-stu-id="7501c-167">The metadata for the new policy assignment.</span></span> <span data-ttu-id="7501c-168">Это может быть путь к имени файла, содержащего метаданные, или метаданные в виде строки.</span><span class="sxs-lookup"><span data-stu-id="7501c-168">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="7501c-169">-Name</span><span class="sxs-lookup"><span data-stu-id="7501c-169">-Name</span></span>
<span data-ttu-id="7501c-170">Указывает имя назначения политики.</span><span class="sxs-lookup"><span data-stu-id="7501c-170">Specifies a name for the policy assignment.</span></span>

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

### <span data-ttu-id="7501c-171">-NotScope</span><span class="sxs-lookup"><span data-stu-id="7501c-171">-NotScope</span></span>
<span data-ttu-id="7501c-172">Области назначения политики не являются.</span><span class="sxs-lookup"><span data-stu-id="7501c-172">The not scopes for policy assignment.</span></span>

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

### <span data-ttu-id="7501c-173">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7501c-173">-PolicyDefinition</span></span>
<span data-ttu-id="7501c-174">Политика в качестве объекта **PsPolicyDefinition,** который содержит правило политики.</span><span class="sxs-lookup"><span data-stu-id="7501c-174">Specifies a policy, as a **PsPolicyDefinition** object that contains the policy rule.</span></span>

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

### <span data-ttu-id="7501c-175">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="7501c-175">-PolicyParameter</span></span>
<span data-ttu-id="7501c-176">Путь к файлу параметра политики или строка параметра политики.</span><span class="sxs-lookup"><span data-stu-id="7501c-176">The policy parameter file path or policy parameter string.</span></span>

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

### <span data-ttu-id="7501c-177">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="7501c-177">-PolicyParameterObject</span></span>
<span data-ttu-id="7501c-178">Объект параметра политики.</span><span class="sxs-lookup"><span data-stu-id="7501c-178">The policy parameter object.</span></span>

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

### <span data-ttu-id="7501c-179">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="7501c-179">-PolicySetDefinition</span></span>
<span data-ttu-id="7501c-180">Объект определения набора политики.</span><span class="sxs-lookup"><span data-stu-id="7501c-180">The policy set definition object.</span></span>

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

### <span data-ttu-id="7501c-181">-Pre</span><span class="sxs-lookup"><span data-stu-id="7501c-181">-Pre</span></span>
<span data-ttu-id="7501c-182">Указывает на то, что этот cmdlet рассматривает предварительные версии API при автоматическом определении используемой версии.</span><span class="sxs-lookup"><span data-stu-id="7501c-182">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="7501c-183">-Scope</span><span class="sxs-lookup"><span data-stu-id="7501c-183">-Scope</span></span>
<span data-ttu-id="7501c-184">Определяет область назначения политики.</span><span class="sxs-lookup"><span data-stu-id="7501c-184">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="7501c-185">Например, чтобы назначить политику группе ресурсов, укажите имя группы ресурсов с `/subscriptions/` ИД `/resourcegroups/` подписки:</span><span class="sxs-lookup"><span data-stu-id="7501c-185">For instance, to assign a policy to a resource group, specify the following: `/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

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

### <span data-ttu-id="7501c-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7501c-186">CommonParameters</span></span>
<span data-ttu-id="7501c-187">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7501c-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7501c-188">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7501c-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7501c-189">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7501c-189">INPUTS</span></span>

### <span data-ttu-id="7501c-190">System.String</span><span class="sxs-lookup"><span data-stu-id="7501c-190">System.String</span></span>

### <span data-ttu-id="7501c-191">System.String[]</span><span class="sxs-lookup"><span data-stu-id="7501c-191">System.String[]</span></span>

### <span data-ttu-id="7501c-192">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="7501c-192">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="7501c-193">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7501c-193">OUTPUTS</span></span>

### <span data-ttu-id="7501c-194">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="7501c-194">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="7501c-195">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7501c-195">NOTES</span></span>

## <span data-ttu-id="7501c-196">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7501c-196">RELATED LINKS</span></span>

[<span data-ttu-id="7501c-197">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7501c-197">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="7501c-198">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="7501c-198">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="7501c-199">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="7501c-199">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="7501c-200">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="7501c-200">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)

