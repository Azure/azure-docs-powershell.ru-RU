---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
ms.openlocfilehash: 5d83266e341643adc45a2fc7af8eff1f9a5e0b3b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905514"
---
# <span data-ttu-id="fda2c-101">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="fda2c-101">Set-AzPolicyAssignment</span></span>

## <span data-ttu-id="fda2c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fda2c-102">SYNOPSIS</span></span>
<span data-ttu-id="fda2c-103">Изменение назначения политики.</span><span class="sxs-lookup"><span data-stu-id="fda2c-103">Modifies a policy assignment.</span></span>

## <span data-ttu-id="fda2c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fda2c-104">SYNTAX</span></span>

### <span data-ttu-id="fda2c-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fda2c-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fda2c-106">PolicyParameterNameObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fda2c-106">PolicyParameterNameObjectParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity]
 [-Location <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fda2c-107">PolicyParameterNameStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="fda2c-107">PolicyParameterNameStringParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fda2c-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fda2c-108">IdParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fda2c-109">PolicyParameterIdObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fda2c-109">PolicyParameterIdObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fda2c-110">PolicyParameterIdStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="fda2c-110">PolicyParameterIdStringParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fda2c-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fda2c-111">DESCRIPTION</span></span>
<span data-ttu-id="fda2c-112">Командлет **Set-AzPolicyAssignment** изменяет назначение политики.</span><span class="sxs-lookup"><span data-stu-id="fda2c-112">The **Set-AzPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="fda2c-113">Укажите назначение по ИДЕНТИФИКАТОРу или по имени и области.</span><span class="sxs-lookup"><span data-stu-id="fda2c-113">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="fda2c-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fda2c-114">EXAMPLES</span></span>

### <span data-ttu-id="fda2c-115">Пример 1: обновление отображаемого имени</span><span class="sxs-lookup"><span data-stu-id="fda2c-115">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="fda2c-116">Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью командлета Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fda2c-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="fda2c-117">Команда сохраняет этот объект в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fda2c-117">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="fda2c-118">Вторая команда получает назначение политики с именем PolicyAssignment с помощью командлета Get-AzPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="fda2c-118">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="fda2c-119">Команда сохраняет этот объект в переменной $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="fda2c-119">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="fda2c-120">Последняя команда обновляет отображаемое имя в назначении политики для группы ресурсов, определяемой свойством **ResourceId** для $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fda2c-120">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="fda2c-121">Пример 2: Добавление управляемого удостоверения в назначение политики</span><span class="sxs-lookup"><span data-stu-id="fda2c-121">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="fda2c-122">Первая команда получает назначение политики с именем PolicyAssignment из текущей подписки с помощью командлета Get-AzPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="fda2c-122">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="fda2c-123">Команда сохраняет этот объект в переменной $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="fda2c-123">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="fda2c-124">Последняя команда назначает управляемое удостоверение для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="fda2c-124">The final command assigns a managed identity to the policy assignment.</span></span>

### <span data-ttu-id="fda2c-125">Пример 3: Обновление параметров назначения политики с помощью нового объекта параметра политики</span><span class="sxs-lookup"><span data-stu-id="fda2c-125">Example 3: Update policy assignment parameters with new policy parameter object</span></span>
```
PS C:\> $Locations = Get-AzLocation | where {($_.displayname -like 'france*') -or ($_.displayname -like 'uk*')}
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="fda2c-126">Первая и вторая команды создают объект, содержащий все регионы Azure, имена которых начинаются с "Франция" или "Великобритания".</span><span class="sxs-lookup"><span data-stu-id="fda2c-126">The first and second commands create an object containing all Azure regions whose names start with "france" or "uk".</span></span>
<span data-ttu-id="fda2c-127">Вторая команда сохраняет этот объект в переменной $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="fda2c-127">The second command stores that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="fda2c-128">Третья команда получает назначение политики с именем "PolicyAssignment" команда сохраняет этот объект в переменной $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="fda2c-128">The third command gets the policy assignment named 'PolicyAssignment' The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="fda2c-129">Последняя команда обновляет значения параметров для назначения политики с именем PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="fda2c-129">The final command updates the parameter values on the policy assignment named PolicyAssignment.</span></span>

### <span data-ttu-id="fda2c-130">Пример 4: Обновление параметров назначения политики с помощью файла параметров политики</span><span class="sxs-lookup"><span data-stu-id="fda2c-130">Example 4: Update policy assignment parameters with policy parameter file</span></span>
<span data-ttu-id="fda2c-131">Создайте файл с именем _AllowedLocations.js_ в локальном рабочем каталоге со следующим содержимым.</span><span class="sxs-lookup"><span data-stu-id="fda2c-131">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="fda2c-132">Команда обновляет назначение политики с именем "PolicyAssignment" с помощью файла параметров политики, AllowedLocations.jsс локального рабочего каталога.</span><span class="sxs-lookup"><span data-stu-id="fda2c-132">The command updates the policy assignment named 'PolicyAssignment' using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

## <span data-ttu-id="fda2c-133">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fda2c-133">PARAMETERS</span></span>

### <span data-ttu-id="fda2c-134">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="fda2c-134">-ApiVersion</span></span>
<span data-ttu-id="fda2c-135">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fda2c-135">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="fda2c-136">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="fda2c-136">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="fda2c-137">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="fda2c-137">-AssignIdentity</span></span>
<span data-ttu-id="fda2c-138">Создание и назначение удостоверения Azure Active Directory для этого назначения политики.</span><span class="sxs-lookup"><span data-stu-id="fda2c-138">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="fda2c-139">Удостоверение будет использоваться при выполнении развертываний для политик "deployIfNotExists".</span><span class="sxs-lookup"><span data-stu-id="fda2c-139">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="fda2c-140">При назначении удостоверения требуется указать расположение.</span><span class="sxs-lookup"><span data-stu-id="fda2c-140">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="fda2c-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fda2c-141">-DefaultProfile</span></span>
<span data-ttu-id="fda2c-142">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="fda2c-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fda2c-143">-Описание</span><span class="sxs-lookup"><span data-stu-id="fda2c-143">-Description</span></span>
<span data-ttu-id="fda2c-144">Описание назначения политики</span><span class="sxs-lookup"><span data-stu-id="fda2c-144">The description for policy assignment</span></span>

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

### <span data-ttu-id="fda2c-145">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="fda2c-145">-DisplayName</span></span>
<span data-ttu-id="fda2c-146">Задает новое отображаемое имя для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="fda2c-146">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="fda2c-147">-ID</span><span class="sxs-lookup"><span data-stu-id="fda2c-147">-Id</span></span>
<span data-ttu-id="fda2c-148">Указывает полный идентификатор ресурса для назначения политики, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="fda2c-148">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="fda2c-149">-Location</span><span class="sxs-lookup"><span data-stu-id="fda2c-149">-Location</span></span>
<span data-ttu-id="fda2c-150">Расположение удостоверения ресурса для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="fda2c-150">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="fda2c-151">Это необходимо, если используется параметр-AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="fda2c-151">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="fda2c-152">-Metadata</span><span class="sxs-lookup"><span data-stu-id="fda2c-152">-Metadata</span></span>
<span data-ttu-id="fda2c-153">Обновленные метаданные для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="fda2c-153">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="fda2c-154">Это может быть либо путь к имени файла, содержащему метаданные, либо метаданные в виде строки.</span><span class="sxs-lookup"><span data-stu-id="fda2c-154">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="fda2c-155">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fda2c-155">-Name</span></span>
<span data-ttu-id="fda2c-156">Указывает имя назначения политики, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="fda2c-156">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="fda2c-157">-NotScope</span><span class="sxs-lookup"><span data-stu-id="fda2c-157">-NotScope</span></span>
<span data-ttu-id="fda2c-158">Назначение политики не является областью действия.</span><span class="sxs-lookup"><span data-stu-id="fda2c-158">The policy assignment not scopes.</span></span>

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

### <span data-ttu-id="fda2c-159">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="fda2c-159">-PolicyParameter</span></span>
<span data-ttu-id="fda2c-160">Новый путь к файлу параметров политики или строковое значение для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="fda2c-160">The new policy parameters file path or string for the policy assignment.</span></span>

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

### <span data-ttu-id="fda2c-161">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="fda2c-161">-PolicyParameterObject</span></span>
<span data-ttu-id="fda2c-162">Новый объект параметров политики для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="fda2c-162">The new policy parameters object for the policy assignment.</span></span>

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

### <span data-ttu-id="fda2c-163">-Pre</span><span class="sxs-lookup"><span data-stu-id="fda2c-163">-Pre</span></span>
<span data-ttu-id="fda2c-164">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="fda2c-164">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="fda2c-165">-Scope</span><span class="sxs-lookup"><span data-stu-id="fda2c-165">-Scope</span></span>
<span data-ttu-id="fda2c-166">Указывает область применения политики.</span><span class="sxs-lookup"><span data-stu-id="fda2c-166">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="fda2c-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fda2c-167">CommonParameters</span></span>
<span data-ttu-id="fda2c-168">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fda2c-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fda2c-169">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fda2c-169">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fda2c-170">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fda2c-170">INPUTS</span></span>

### <span data-ttu-id="fda2c-171">System. String</span><span class="sxs-lookup"><span data-stu-id="fda2c-171">System.String</span></span>

### <span data-ttu-id="fda2c-172">System. String []</span><span class="sxs-lookup"><span data-stu-id="fda2c-172">System.String[]</span></span>

## <span data-ttu-id="fda2c-173">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fda2c-173">OUTPUTS</span></span>

### <span data-ttu-id="fda2c-174">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="fda2c-174">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="fda2c-175">Пуск</span><span class="sxs-lookup"><span data-stu-id="fda2c-175">NOTES</span></span>

## <span data-ttu-id="fda2c-176">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fda2c-176">RELATED LINKS</span></span>

[<span data-ttu-id="fda2c-177">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="fda2c-177">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="fda2c-178">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="fda2c-178">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="fda2c-179">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="fda2c-179">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)


