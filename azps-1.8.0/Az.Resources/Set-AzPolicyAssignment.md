---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
ms.openlocfilehash: 2b699219281d64e50694f7e7dd70a965626f7132
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729316"
---
# <span data-ttu-id="b43cf-101">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b43cf-101">Set-AzPolicyAssignment</span></span>

## <span data-ttu-id="b43cf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b43cf-102">SYNOPSIS</span></span>
<span data-ttu-id="b43cf-103">Изменение назначения политики.</span><span class="sxs-lookup"><span data-stu-id="b43cf-103">Modifies a policy assignment.</span></span>

## <span data-ttu-id="b43cf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b43cf-104">SYNTAX</span></span>

### <span data-ttu-id="b43cf-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b43cf-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b43cf-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b43cf-106">IdParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b43cf-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b43cf-107">DESCRIPTION</span></span>
<span data-ttu-id="b43cf-108">Командлет **Set-AzPolicyAssignment** изменяет назначение политики.</span><span class="sxs-lookup"><span data-stu-id="b43cf-108">The **Set-AzPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="b43cf-109">Укажите назначение по ИДЕНТИФИКАТОРу или по имени и области.</span><span class="sxs-lookup"><span data-stu-id="b43cf-109">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="b43cf-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b43cf-110">EXAMPLES</span></span>

### <span data-ttu-id="b43cf-111">Пример 1: обновление отображаемого имени</span><span class="sxs-lookup"><span data-stu-id="b43cf-111">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="b43cf-112">Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью командлета Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b43cf-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="b43cf-113">Команда сохраняет этот объект в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b43cf-113">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="b43cf-114">Вторая команда получает назначение политики с именем PolicyAssignment с помощью командлета Get-AzPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="b43cf-114">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="b43cf-115">Команда сохраняет этот объект в переменной $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="b43cf-115">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="b43cf-116">Последняя команда обновляет отображаемое имя в назначении политики для группы ресурсов, определяемой свойством **ResourceId** для $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b43cf-116">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="b43cf-117">Пример 2: Добавление управляемого удостоверения в назначение политики</span><span class="sxs-lookup"><span data-stu-id="b43cf-117">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="b43cf-118">Первая команда получает назначение политики с именем PolicyAssignment из текущей подписки с помощью командлета Get-AzPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="b43cf-118">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="b43cf-119">Команда сохраняет этот объект в переменной $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="b43cf-119">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="b43cf-120">Последняя команда назначает управляемое удостоверение для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="b43cf-120">The final command assigns a managed identity to the policy assignment.</span></span>

## <span data-ttu-id="b43cf-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b43cf-121">PARAMETERS</span></span>

### <span data-ttu-id="b43cf-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b43cf-122">-ApiVersion</span></span>
<span data-ttu-id="b43cf-123">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b43cf-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="b43cf-124">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="b43cf-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="b43cf-125">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="b43cf-125">-AssignIdentity</span></span>
<span data-ttu-id="b43cf-126">Создание и назначение удостоверения Azure Active Directory для этого назначения политики.</span><span class="sxs-lookup"><span data-stu-id="b43cf-126">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="b43cf-127">Удостоверение будет использоваться при выполнении развертываний для политик "deployIfNotExists".</span><span class="sxs-lookup"><span data-stu-id="b43cf-127">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="b43cf-128">При назначении удостоверения требуется указать расположение.</span><span class="sxs-lookup"><span data-stu-id="b43cf-128">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="b43cf-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b43cf-129">-DefaultProfile</span></span>
<span data-ttu-id="b43cf-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b43cf-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b43cf-131">-Описание</span><span class="sxs-lookup"><span data-stu-id="b43cf-131">-Description</span></span>
<span data-ttu-id="b43cf-132">Описание назначения политики</span><span class="sxs-lookup"><span data-stu-id="b43cf-132">The description for policy assignment</span></span>

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

### <span data-ttu-id="b43cf-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b43cf-133">-DisplayName</span></span>
<span data-ttu-id="b43cf-134">Задает новое отображаемое имя для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="b43cf-134">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="b43cf-135">-ID</span><span class="sxs-lookup"><span data-stu-id="b43cf-135">-Id</span></span>
<span data-ttu-id="b43cf-136">Указывает полный идентификатор ресурса для назначения политики, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b43cf-136">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="b43cf-137">-Location</span><span class="sxs-lookup"><span data-stu-id="b43cf-137">-Location</span></span>
<span data-ttu-id="b43cf-138">Расположение удостоверения ресурса для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="b43cf-138">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="b43cf-139">Это необходимо, если используется параметр-AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="b43cf-139">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="b43cf-140">-Metadata</span><span class="sxs-lookup"><span data-stu-id="b43cf-140">-Metadata</span></span>
<span data-ttu-id="b43cf-141">Обновленные метаданные для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="b43cf-141">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="b43cf-142">Это может быть либо путь к имени файла, содержащему метаданные, либо метаданные в виде строки.</span><span class="sxs-lookup"><span data-stu-id="b43cf-142">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="b43cf-143">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b43cf-143">-Name</span></span>
<span data-ttu-id="b43cf-144">Указывает имя назначения политики, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b43cf-144">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b43cf-145">-NotScope</span><span class="sxs-lookup"><span data-stu-id="b43cf-145">-NotScope</span></span>
<span data-ttu-id="b43cf-146">Назначение политики не является областью действия.</span><span class="sxs-lookup"><span data-stu-id="b43cf-146">The policy assignment not scopes.</span></span>

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

### <span data-ttu-id="b43cf-147">-Pre</span><span class="sxs-lookup"><span data-stu-id="b43cf-147">-Pre</span></span>
<span data-ttu-id="b43cf-148">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="b43cf-148">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b43cf-149">-Scope</span><span class="sxs-lookup"><span data-stu-id="b43cf-149">-Scope</span></span>
<span data-ttu-id="b43cf-150">Указывает область применения политики.</span><span class="sxs-lookup"><span data-stu-id="b43cf-150">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b43cf-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b43cf-151">CommonParameters</span></span>
<span data-ttu-id="b43cf-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b43cf-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b43cf-153">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b43cf-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b43cf-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b43cf-154">INPUTS</span></span>

### <span data-ttu-id="b43cf-155">System. String</span><span class="sxs-lookup"><span data-stu-id="b43cf-155">System.String</span></span>

### <span data-ttu-id="b43cf-156">System. String []</span><span class="sxs-lookup"><span data-stu-id="b43cf-156">System.String[]</span></span>

## <span data-ttu-id="b43cf-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b43cf-157">OUTPUTS</span></span>

### <span data-ttu-id="b43cf-158">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="b43cf-158">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="b43cf-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="b43cf-159">NOTES</span></span>

## <span data-ttu-id="b43cf-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b43cf-160">RELATED LINKS</span></span>

[<span data-ttu-id="b43cf-161">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b43cf-161">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="b43cf-162">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b43cf-162">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="b43cf-163">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b43cf-163">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)


