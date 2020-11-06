---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
ms.openlocfilehash: 364411d6b69c04d8b29c1c32e2809ec3c4789b09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566910"
---
# <span data-ttu-id="ee801-101">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="ee801-101">New-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="ee801-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ee801-102">SYNOPSIS</span></span>
<span data-ttu-id="ee801-103">Создание назначения политики.</span><span class="sxs-lookup"><span data-stu-id="ee801-103">Creates a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee801-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ee801-104">SYNTAX</span></span>

### <span data-ttu-id="ee801-105">CreateWithoutParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ee801-105">CreateWithoutParameters (Default)</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Sku <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ee801-106">CreateWithPolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="ee801-106">CreateWithPolicyParameterObject</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ee801-107">CreateWithPolicyParameterString</span><span class="sxs-lookup"><span data-stu-id="ee801-107">CreateWithPolicyParameterString</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ee801-108">CreateWithPolicySetParameterObject</span><span class="sxs-lookup"><span data-stu-id="ee801-108">CreateWithPolicySetParameterObject</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ee801-109">CreateWithPolicySetParameterString</span><span class="sxs-lookup"><span data-stu-id="ee801-109">CreateWithPolicySetParameterString</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ee801-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee801-110">DESCRIPTION</span></span>
<span data-ttu-id="ee801-111">Командлет **New-AzureRmPolicyAssignment** создает назначение политики.</span><span class="sxs-lookup"><span data-stu-id="ee801-111">The **New-AzureRmPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="ee801-112">Укажите политику и область действия.</span><span class="sxs-lookup"><span data-stu-id="ee801-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="ee801-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ee801-113">EXAMPLES</span></span>

### <span data-ttu-id="ee801-114">Пример 1: назначение политики на уровне группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ee801-114">Example 1: Policy assignment at resource group level</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $Policy = Get-AzureRmPolicyDefinition -Name "VirtualMachinePolicy"
PS C:\> New-AzureRmPolicyAssignment -Name "VirtualMachinePolicyAssignment" -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="ee801-115">Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью командлета Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ee801-115">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="ee801-116">Команда сохраняет этот объект в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ee801-116">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="ee801-117">Вторая команда получает определение политики с именем VirtualMachinePolicy с помощью командлета Get-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="ee801-117">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="ee801-118">Команда сохраняет этот объект в переменной $Policy.</span><span class="sxs-lookup"><span data-stu-id="ee801-118">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="ee801-119">Последняя команда назначает политику в $Policy на уровне группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ee801-119">The final command assigns the policy in $Policy at the level of a resource group.</span></span>
<span data-ttu-id="ee801-120">Свойство **ResourceId** для $ResourceGroup определяет группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ee801-120">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="ee801-121">Пример 2: назначение политики на уровне группы ресурсов с объектом параметра политики</span><span class="sxs-lookup"><span data-stu-id="ee801-121">Example 2: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $Policy = Get-AzureRmPolicyDefinition | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations' -and $_.Properties.PolicyType -eq 'BuiltIn'}
PS C:\> $Locations = Get-AzureRmLocation | where displayname -like "*east*"
PS C:\> $AllowedLocations = @{"listOfAllowedLocations"=($Locations.location)}
PS C:\> New-AzureRmPolicyAssignment -Name "RestrictLocationPolicyAssignment" -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="ee801-122">Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью командлета Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ee801-122">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="ee801-123">Команда сохраняет этот объект в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ee801-123">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="ee801-124">Вторая команда получает встроенное определение политики для допустимых местоположений с помощью командлета Get-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="ee801-124">The second command gets the built-in policy definition for allowed locations by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="ee801-125">Команда сохраняет этот объект в переменной $Policy.</span><span class="sxs-lookup"><span data-stu-id="ee801-125">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="ee801-126">Третья и четвертая команды создают объект, содержащий все регионы Azure с именем "Восток".</span><span class="sxs-lookup"><span data-stu-id="ee801-126">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="ee801-127">Команды хранят этот объект в переменной $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="ee801-127">The commands store that object in the $AllowedLocations variable.</span></span>

<span data-ttu-id="ee801-128">Последняя команда назначает политику в $Policy на уровне группы ресурсов, используя объект параметра политики в $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="ee801-128">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="ee801-129">Свойство **ResourceId** для $ResourceGroup определяет группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ee801-129">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="ee801-130">Пример 3: назначение политики на уровне группы ресурсов с помощью файла параметров политики</span><span class="sxs-lookup"><span data-stu-id="ee801-130">Example 3: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="ee801-131">Создайте файл с именем _AllowedLocations.js_ в локальном рабочем каталоге со следующим содержимым.</span><span class="sxs-lookup"><span data-stu-id="ee801-131">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>
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
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $Policy = Get-AzureRmPolicyDefinition | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations' -and $_.Properties.PolicyType -eq 'BuiltIn'}
PS C:\> New-AzureRmPolicyAssignment -Name "RestrictLocationPolicyAssignment" -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameter .\AllowedLocations.json
```

<span data-ttu-id="ee801-132">Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью командлета Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ee801-132">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="ee801-133">Команда сохраняет этот объект в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ee801-133">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="ee801-134">Вторая команда получает встроенное определение политики для допустимых местоположений с помощью командлета Get-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="ee801-134">The second command gets the built-in policy definition for allowed locations by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="ee801-135">Команда сохраняет этот объект в переменной $Policy.</span><span class="sxs-lookup"><span data-stu-id="ee801-135">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="ee801-136">Последняя команда назначает политику на уровне $Policy в группе ресурсов с помощью файла параметров политики AllowedLocations.json из локального рабочего каталога.</span><span class="sxs-lookup"><span data-stu-id="ee801-136">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter file AllowedLocations.json from the local working directory.</span></span>
<span data-ttu-id="ee801-137">Свойство **ResourceId** для $ResourceGroup определяет группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ee801-137">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>


## <span data-ttu-id="ee801-138">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ee801-138">PARAMETERS</span></span>

### <span data-ttu-id="ee801-139">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ee801-139">-ApiVersion</span></span>
<span data-ttu-id="ee801-140">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ee801-140">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="ee801-141">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="ee801-141">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee801-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee801-142">-DefaultProfile</span></span>
<span data-ttu-id="ee801-143">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ee801-143">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee801-144">-Описание</span><span class="sxs-lookup"><span data-stu-id="ee801-144">-Description</span></span>
<span data-ttu-id="ee801-145">Описание назначения политики</span><span class="sxs-lookup"><span data-stu-id="ee801-145">The description for policy assignment</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee801-146">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ee801-146">-DisplayName</span></span>
<span data-ttu-id="ee801-147">Задает отображаемое имя для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="ee801-147">Specifies a display name for the policy assignment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee801-148">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ee801-148">-InformationAction</span></span>
<span data-ttu-id="ee801-149">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="ee801-149">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ee801-150">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ee801-150">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ee801-151">Продолжал</span><span class="sxs-lookup"><span data-stu-id="ee801-151">Continue</span></span>
- <span data-ttu-id="ee801-152">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="ee801-152">Ignore</span></span>
- <span data-ttu-id="ee801-153">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="ee801-153">Inquire</span></span>
- <span data-ttu-id="ee801-154">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ee801-154">SilentlyContinue</span></span>
- <span data-ttu-id="ee801-155">Остановить</span><span class="sxs-lookup"><span data-stu-id="ee801-155">Stop</span></span>
- <span data-ttu-id="ee801-156">Рвать</span><span class="sxs-lookup"><span data-stu-id="ee801-156">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee801-157">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ee801-157">-InformationVariable</span></span>
<span data-ttu-id="ee801-158">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="ee801-158">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee801-159">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ee801-159">-Name</span></span>
<span data-ttu-id="ee801-160">Задает имя для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="ee801-160">Specifies a name for the policy assignment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee801-161">-NotScope</span><span class="sxs-lookup"><span data-stu-id="ee801-161">-NotScope</span></span>
<span data-ttu-id="ee801-162">Область "не для назначения политики".</span><span class="sxs-lookup"><span data-stu-id="ee801-162">The not scopes for policy assignment.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee801-163">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ee801-163">-PolicyDefinition</span></span>
<span data-ttu-id="ee801-164">Указывает политику, как объект **PSObject** , который содержит правило политики.</span><span class="sxs-lookup"><span data-stu-id="ee801-164">Specifies a policy, as a **PSObject** object that contains the policy rule.</span></span>

```yaml
Type: PSObject
Parameter Sets: CreateWithoutParameters, CreateWithPolicySetParameterObject, CreateWithPolicySetParameterString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: PSObject
Parameter Sets: CreateWithPolicyParameterObject, CreateWithPolicyParameterString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee801-165">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="ee801-165">-PolicyParameter</span></span>
<span data-ttu-id="ee801-166">Путь к файлу параметра политики или строка параметра политики.</span><span class="sxs-lookup"><span data-stu-id="ee801-166">The policy parameter file path or policy parameter string.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithPolicyParameterString, CreateWithPolicySetParameterString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee801-167">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="ee801-167">-PolicyParameterObject</span></span>
<span data-ttu-id="ee801-168">Объект параметра политики.</span><span class="sxs-lookup"><span data-stu-id="ee801-168">The policy parameter object.</span></span>

```yaml
Type: Hashtable
Parameter Sets: CreateWithPolicyParameterObject, CreateWithPolicySetParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee801-169">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="ee801-169">-PolicySetDefinition</span></span>
<span data-ttu-id="ee801-170">Объект определения параметра политики.</span><span class="sxs-lookup"><span data-stu-id="ee801-170">The policy set definition object.</span></span>

```yaml
Type: PSObject
Parameter Sets: CreateWithoutParameters, CreateWithPolicyParameterObject, CreateWithPolicyParameterString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: PSObject
Parameter Sets: CreateWithPolicySetParameterObject, CreateWithPolicySetParameterString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee801-171">-Pre</span><span class="sxs-lookup"><span data-stu-id="ee801-171">-Pre</span></span>
<span data-ttu-id="ee801-172">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="ee801-172">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee801-173">-Scope</span><span class="sxs-lookup"><span data-stu-id="ee801-173">-Scope</span></span>
<span data-ttu-id="ee801-174">Указывает область, в которой нужно назначить политику.</span><span class="sxs-lookup"><span data-stu-id="ee801-174">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="ee801-175">Например, чтобы назначить политику группе ресурсов, укажите следующее:</span><span class="sxs-lookup"><span data-stu-id="ee801-175">For instance, to assign a policy to a resource group, specify the following:</span></span>

<span data-ttu-id="ee801-176">`/subscriptions/``/resourcegroups/`имя группы ресурсов для идентификатора подписки</span><span class="sxs-lookup"><span data-stu-id="ee801-176">`/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee801-177">-SKU</span><span class="sxs-lookup"><span data-stu-id="ee801-177">-Sku</span></span>
<span data-ttu-id="ee801-178">Хэш-таблица, представляющая свойства SKU.</span><span class="sxs-lookup"><span data-stu-id="ee801-178">A hash table which represents sku properties.</span></span> <span data-ttu-id="ee801-179">По умолчанию для освобождения SKU: Name = a0, Tier = fre</span><span class="sxs-lookup"><span data-stu-id="ee801-179">Defaults to Free Sku: Name = A0, Tier = Fre</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee801-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee801-180">CommonParameters</span></span>
<span data-ttu-id="ee801-181">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ee801-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee801-182">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee801-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee801-183">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ee801-183">INPUTS</span></span>

### <span data-ttu-id="ee801-184">Ничего</span><span class="sxs-lookup"><span data-stu-id="ee801-184">None</span></span>
<span data-ttu-id="ee801-185">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="ee801-185">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ee801-186">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee801-186">OUTPUTS</span></span>

### <span data-ttu-id="ee801-187">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="ee801-187">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="ee801-188">Пуск</span><span class="sxs-lookup"><span data-stu-id="ee801-188">NOTES</span></span>

## <span data-ttu-id="ee801-189">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ee801-189">RELATED LINKS</span></span>

[<span data-ttu-id="ee801-190">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ee801-190">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="ee801-191">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="ee801-191">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="ee801-192">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="ee801-192">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="ee801-193">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="ee801-193">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


