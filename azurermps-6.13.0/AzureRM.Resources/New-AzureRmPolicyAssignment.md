---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
ms.openlocfilehash: 616b75b4bdc5dab9f02bb1fc295effefc0e728be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556511"
---
# <span data-ttu-id="0f76b-101">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="0f76b-101">New-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="0f76b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0f76b-102">SYNOPSIS</span></span>
<span data-ttu-id="0f76b-103">Создание назначения политики.</span><span class="sxs-lookup"><span data-stu-id="0f76b-103">Creates a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f76b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0f76b-104">SYNTAX</span></span>

### <span data-ttu-id="0f76b-105">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0f76b-105">DefaultParameterSet (Default)</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Metadata <String>]
 [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="0f76b-106">PolicyParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f76b-106">PolicyParameterObjectParameterSet</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity]
 [-Location <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="0f76b-107">PolicyParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f76b-107">PolicyParameterStringParameterSet</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="0f76b-108">PolicySetParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f76b-108">PolicySetParameterObjectParameterSet</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity]
 [-Location <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="0f76b-109">PolicySetParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f76b-109">PolicySetParameterStringParameterSet</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="0f76b-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f76b-110">DESCRIPTION</span></span>
<span data-ttu-id="0f76b-111">Командлет **New-AzureRmPolicyAssignment** создает назначение политики.</span><span class="sxs-lookup"><span data-stu-id="0f76b-111">The **New-AzureRmPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="0f76b-112">Укажите политику и область действия.</span><span class="sxs-lookup"><span data-stu-id="0f76b-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="0f76b-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0f76b-113">EXAMPLES</span></span>

### <span data-ttu-id="0f76b-114">Пример 1: назначение политики на уровне группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="0f76b-114">Example 1: Policy assignment at resource group level</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzureRmPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzureRmPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="0f76b-115">Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью командлета Get-AzureRMResourceGroup и сохраняет его в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="0f76b-115">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="0f76b-116">Вторая команда получает определение политики с именем VirtualMachinePolicy с помощью командлета Get-AzureRmPolicyDefinition и сохраняет его в переменной $Policy.</span><span class="sxs-lookup"><span data-stu-id="0f76b-116">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzureRmPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="0f76b-117">Последняя команда назначает политику в $Policy на уровне группы ресурсов, определяемой свойством **ResourceId** $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="0f76b-117">The final command assigns the policy in $Policy at the level of the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="0f76b-118">Пример 2: назначение политики на уровне группы ресурсов с объектом параметра политики</span><span class="sxs-lookup"><span data-stu-id="0f76b-118">Example 2: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzureRmPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> $Locations = Get-AzureRmLocation | where displayname -like '*east*'
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> New-AzureRmPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="0f76b-119">Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью командлета Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="0f76b-119">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="0f76b-120">Команда сохраняет этот объект в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="0f76b-120">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="0f76b-121">Вторая команда получает встроенное определение политики для допустимых местоположений с помощью командлета Get-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="0f76b-121">The second command gets the built-in policy definition for allowed locations by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="0f76b-122">Команда сохраняет этот объект в переменной $Policy.</span><span class="sxs-lookup"><span data-stu-id="0f76b-122">The command stores that object in the $Policy variable.</span></span>
<span data-ttu-id="0f76b-123">Третья и четвертая команды создают объект, содержащий все регионы Azure с именем "Восток".</span><span class="sxs-lookup"><span data-stu-id="0f76b-123">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="0f76b-124">Команды хранят этот объект в переменной $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="0f76b-124">The commands store that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="0f76b-125">Последняя команда назначает политику в $Policy на уровне группы ресурсов, используя объект параметра политики в $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="0f76b-125">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="0f76b-126">Свойство **ResourceId** для $ResourceGroup определяет группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0f76b-126">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="0f76b-127">Пример 3: назначение политики на уровне группы ресурсов с помощью файла параметров политики</span><span class="sxs-lookup"><span data-stu-id="0f76b-127">Example 3: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="0f76b-128">Создайте файл с именем _AllowedLocations.js_ в локальном рабочем каталоге со следующим содержимым.</span><span class="sxs-lookup"><span data-stu-id="0f76b-128">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzureRmPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> New-AzureRmPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameter .\AllowedLocations.json
```

<span data-ttu-id="0f76b-129">Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью командлета Get-AzureRMResourceGroup и сохраняет его в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="0f76b-129">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="0f76b-130">Вторая команда получает встроенное определение политики для допустимых местоположений с помощью командлета Get-AzureRmPolicyDefinition и сохраняет его в переменной $Policy.</span><span class="sxs-lookup"><span data-stu-id="0f76b-130">The second command gets the built-in policy definition for allowed locations by using the Get-AzureRmPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="0f76b-131">Последняя команда назначает политику в $Policy в группе ресурсов, определяемой свойством **ResourceId** $ResourceGroup с помощью файла параметров политики AllowedLocations.json из локального рабочего каталога.</span><span class="sxs-lookup"><span data-stu-id="0f76b-131">The final command assigns the policy in $Policy at the resource group identified by the **ResourceId** property of $ResourceGroup using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="0f76b-132">Пример 4: назначение политики с управляемым удостоверением</span><span class="sxs-lookup"><span data-stu-id="0f76b-132">Example 4: Policy assignment with a managed identity</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzureRmPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzureRmPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -Location 'eastus' -AssignIdentity 
```

<span data-ttu-id="0f76b-133">Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью командлета Get-AzureRMResourceGroup и сохраняет его в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="0f76b-133">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="0f76b-134">Вторая команда получает определение политики с именем VirtualMachinePolicy с помощью командлета Get-AzureRmPolicyDefinition и сохраняет его в переменной $Policy.</span><span class="sxs-lookup"><span data-stu-id="0f76b-134">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzureRmPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="0f76b-135">Последняя команда назначает политику в $Policy группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0f76b-135">The final command assigns the policy in $Policy to the resource group.</span></span> <span data-ttu-id="0f76b-136">Управляемое удостоверение создается автоматически и назначается назначению политики.</span><span class="sxs-lookup"><span data-stu-id="0f76b-136">A managed identity is automatically created and assigned to the policy assignment.</span></span>

## <span data-ttu-id="0f76b-137">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0f76b-137">PARAMETERS</span></span>

### <span data-ttu-id="0f76b-138">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0f76b-138">-ApiVersion</span></span>
<span data-ttu-id="0f76b-139">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0f76b-139">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="0f76b-140">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="0f76b-140">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="0f76b-141">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="0f76b-141">-AssignIdentity</span></span>
<span data-ttu-id="0f76b-142">Создание и назначение удостоверения Azure Active Directory для этого назначения политики.</span><span class="sxs-lookup"><span data-stu-id="0f76b-142">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="0f76b-143">Удостоверение будет использоваться при выполнении развертываний для политик "deployIfNotExists".</span><span class="sxs-lookup"><span data-stu-id="0f76b-143">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="0f76b-144">При назначении удостоверения требуется указать расположение.</span><span class="sxs-lookup"><span data-stu-id="0f76b-144">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="0f76b-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f76b-145">-DefaultProfile</span></span>
<span data-ttu-id="0f76b-146">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0f76b-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f76b-147">-Описание</span><span class="sxs-lookup"><span data-stu-id="0f76b-147">-Description</span></span>
<span data-ttu-id="0f76b-148">Описание назначения политики</span><span class="sxs-lookup"><span data-stu-id="0f76b-148">The description for policy assignment</span></span>

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

### <span data-ttu-id="0f76b-149">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0f76b-149">-DisplayName</span></span>
<span data-ttu-id="0f76b-150">Задает отображаемое имя для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="0f76b-150">Specifies a display name for the policy assignment.</span></span>

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

### <span data-ttu-id="0f76b-151">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="0f76b-151">-InformationAction</span></span>
<span data-ttu-id="0f76b-152">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="0f76b-152">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="0f76b-153">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0f76b-153">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0f76b-154">Продолжал</span><span class="sxs-lookup"><span data-stu-id="0f76b-154">Continue</span></span>
- <span data-ttu-id="0f76b-155">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="0f76b-155">Ignore</span></span>
- <span data-ttu-id="0f76b-156">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="0f76b-156">Inquire</span></span>
- <span data-ttu-id="0f76b-157">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0f76b-157">SilentlyContinue</span></span>
- <span data-ttu-id="0f76b-158">Остановить</span><span class="sxs-lookup"><span data-stu-id="0f76b-158">Stop</span></span>
- <span data-ttu-id="0f76b-159">Рвать</span><span class="sxs-lookup"><span data-stu-id="0f76b-159">Suspend</span></span>

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

### <span data-ttu-id="0f76b-160">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0f76b-160">-InformationVariable</span></span>
<span data-ttu-id="0f76b-161">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="0f76b-161">Specifies an information variable.</span></span>

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

### <span data-ttu-id="0f76b-162">-Location</span><span class="sxs-lookup"><span data-stu-id="0f76b-162">-Location</span></span>
<span data-ttu-id="0f76b-163">Расположение удостоверения ресурса для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="0f76b-163">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="0f76b-164">Это необходимо, если используется параметр-AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="0f76b-164">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="0f76b-165">-Metadata</span><span class="sxs-lookup"><span data-stu-id="0f76b-165">-Metadata</span></span>
<span data-ttu-id="0f76b-166">Метаданные для нового назначения политики.</span><span class="sxs-lookup"><span data-stu-id="0f76b-166">The metadata for the new policy assignment.</span></span> <span data-ttu-id="0f76b-167">Это может быть либо путь к имени файла, содержащему метаданные, либо метаданные в виде строки.</span><span class="sxs-lookup"><span data-stu-id="0f76b-167">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="0f76b-168">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0f76b-168">-Name</span></span>
<span data-ttu-id="0f76b-169">Задает имя для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="0f76b-169">Specifies a name for the policy assignment.</span></span>

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

### <span data-ttu-id="0f76b-170">-NotScope</span><span class="sxs-lookup"><span data-stu-id="0f76b-170">-NotScope</span></span>
<span data-ttu-id="0f76b-171">Область "не для назначения политики".</span><span class="sxs-lookup"><span data-stu-id="0f76b-171">The not scopes for policy assignment.</span></span>

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

### <span data-ttu-id="0f76b-172">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0f76b-172">-PolicyDefinition</span></span>
<span data-ttu-id="0f76b-173">Указывает политику как объект **PsPolicyDefinition** , который содержит правило политики.</span><span class="sxs-lookup"><span data-stu-id="0f76b-173">Specifies a policy, as a **PsPolicyDefinition** object that contains the policy rule.</span></span>

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

### <span data-ttu-id="0f76b-174">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="0f76b-174">-PolicyParameter</span></span>
<span data-ttu-id="0f76b-175">Путь к файлу параметра политики или строка параметра политики.</span><span class="sxs-lookup"><span data-stu-id="0f76b-175">The policy parameter file path or policy parameter string.</span></span>

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

### <span data-ttu-id="0f76b-176">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="0f76b-176">-PolicyParameterObject</span></span>
<span data-ttu-id="0f76b-177">Объект параметра политики.</span><span class="sxs-lookup"><span data-stu-id="0f76b-177">The policy parameter object.</span></span>

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

### <span data-ttu-id="0f76b-178">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="0f76b-178">-PolicySetDefinition</span></span>
<span data-ttu-id="0f76b-179">Объект определения параметра политики.</span><span class="sxs-lookup"><span data-stu-id="0f76b-179">The policy set definition object.</span></span>

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

### <span data-ttu-id="0f76b-180">-Pre</span><span class="sxs-lookup"><span data-stu-id="0f76b-180">-Pre</span></span>
<span data-ttu-id="0f76b-181">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="0f76b-181">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0f76b-182">-Scope</span><span class="sxs-lookup"><span data-stu-id="0f76b-182">-Scope</span></span>
<span data-ttu-id="0f76b-183">Указывает область, в которой нужно назначить политику.</span><span class="sxs-lookup"><span data-stu-id="0f76b-183">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="0f76b-184">Например, чтобы назначить политику группе ресурсов, укажите следующее: `/subscriptions/` `/resourcegroups/` имя группы ресурсов для идентификатора подписки</span><span class="sxs-lookup"><span data-stu-id="0f76b-184">For instance, to assign a policy to a resource group, specify the following: `/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

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

### <span data-ttu-id="0f76b-185">-SKU</span><span class="sxs-lookup"><span data-stu-id="0f76b-185">-Sku</span></span>
<span data-ttu-id="0f76b-186">Хэш-таблица, представляющая свойства SKU.</span><span class="sxs-lookup"><span data-stu-id="0f76b-186">A hash table which represents SKU properties.</span></span> <span data-ttu-id="0f76b-187">По умолчанию используется бесплатная SKU со значениями: `@{Name = 'A0'; Tier = 'Free'}` .</span><span class="sxs-lookup"><span data-stu-id="0f76b-187">Defaults to the Free SKU with the values: `@{Name = 'A0'; Tier = 'Free'}`.</span></span> <span data-ttu-id="0f76b-188">Чтобы использовать стандартную SKU, используйте значения: `@{Name = 'A1'; Tier = 'Standard'}` .</span><span class="sxs-lookup"><span data-stu-id="0f76b-188">To use the Standard SKU, use the values: `@{Name = 'A1'; Tier = 'Standard'}`.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f76b-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f76b-189">CommonParameters</span></span>
<span data-ttu-id="0f76b-190">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0f76b-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f76b-191">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f76b-191">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f76b-192">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0f76b-192">INPUTS</span></span>

## <span data-ttu-id="0f76b-193">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f76b-193">OUTPUTS</span></span>

## <span data-ttu-id="0f76b-194">Пуск</span><span class="sxs-lookup"><span data-stu-id="0f76b-194">NOTES</span></span>

## <span data-ttu-id="0f76b-195">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0f76b-195">RELATED LINKS</span></span>

[<span data-ttu-id="0f76b-196">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0f76b-196">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="0f76b-197">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="0f76b-197">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="0f76b-198">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="0f76b-198">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="0f76b-199">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="0f76b-199">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


