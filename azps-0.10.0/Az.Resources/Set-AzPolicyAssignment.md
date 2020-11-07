---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-Azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzPolicyAssignment.md
ms.openlocfilehash: 102d297f53fe51779f8831e4890c7d55bb59d2eb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910827"
---
# <span data-ttu-id="2f1ba-101">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="2f1ba-101">Set-AzPolicyAssignment</span></span>

## <span data-ttu-id="2f1ba-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2f1ba-102">SYNOPSIS</span></span>
<span data-ttu-id="2f1ba-103">Изменение назначения политики.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-103">Modifies a policy assignment.</span></span>

## <span data-ttu-id="2f1ba-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2f1ba-104">SYNTAX</span></span>

### <span data-ttu-id="2f1ba-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2f1ba-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="2f1ba-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f1ba-106">IdParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2f1ba-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f1ba-107">DESCRIPTION</span></span>
<span data-ttu-id="2f1ba-108">Командлет **Set-AzPolicyAssignment** изменяет назначение политики.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-108">The **Set-AzPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="2f1ba-109">Укажите назначение по ИДЕНТИФИКАТОРу или по имени и области.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-109">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="2f1ba-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2f1ba-110">EXAMPLES</span></span>

### <span data-ttu-id="2f1ba-111">Пример 1: обновление отображаемого имени</span><span class="sxs-lookup"><span data-stu-id="2f1ba-111">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="2f1ba-112">Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью командлета Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="2f1ba-113">Команда сохраняет этот объект в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-113">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="2f1ba-114">Вторая команда получает назначение политики с именем PolicyAssignment с помощью командлета Get-AzPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-114">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="2f1ba-115">Команда сохраняет этот объект в переменной $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-115">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="2f1ba-116">Последняя команда обновляет отображаемое имя в назначении политики для группы ресурсов, определяемой свойством **ResourceId** для $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-116">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="2f1ba-117">Пример 2: Добавление управляемого удостоверения в назначение политики</span><span class="sxs-lookup"><span data-stu-id="2f1ba-117">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="2f1ba-118">Первая команда получает назначение политики с именем PolicyAssignment из текущей подписки с помощью командлета Get-AzPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-118">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="2f1ba-119">Команда сохраняет этот объект в переменной $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-119">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="2f1ba-120">Последняя команда назначает управляемое удостоверение для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-120">The final command assigns a managed identity to the policy assignment.</span></span>

## <span data-ttu-id="2f1ba-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2f1ba-121">PARAMETERS</span></span>

### <span data-ttu-id="2f1ba-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2f1ba-122">-ApiVersion</span></span>
<span data-ttu-id="2f1ba-123">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="2f1ba-124">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="2f1ba-125">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="2f1ba-125">-AssignIdentity</span></span>
<span data-ttu-id="2f1ba-126">Создание и назначение удостоверения Azure Active Directory для этого назначения политики.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-126">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="2f1ba-127">Удостоверение будет использоваться при выполнении развертываний для политик "deployIfNotExists".</span><span class="sxs-lookup"><span data-stu-id="2f1ba-127">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="2f1ba-128">При назначении удостоверения требуется указать расположение.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-128">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="2f1ba-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f1ba-129">-DefaultProfile</span></span>
<span data-ttu-id="2f1ba-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2f1ba-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f1ba-131">-Описание</span><span class="sxs-lookup"><span data-stu-id="2f1ba-131">-Description</span></span>
<span data-ttu-id="2f1ba-132">Описание назначения политики</span><span class="sxs-lookup"><span data-stu-id="2f1ba-132">The description for policy assignment</span></span>

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

### <span data-ttu-id="2f1ba-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2f1ba-133">-DisplayName</span></span>
<span data-ttu-id="2f1ba-134">Задает новое отображаемое имя для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-134">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="2f1ba-135">-ID</span><span class="sxs-lookup"><span data-stu-id="2f1ba-135">-Id</span></span>
<span data-ttu-id="2f1ba-136">Указывает полный идентификатор ресурса для назначения политики, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-136">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="2f1ba-137">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2f1ba-137">-InformationAction</span></span>
<span data-ttu-id="2f1ba-138">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-138">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="2f1ba-139">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="2f1ba-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2f1ba-140">Продолжал</span><span class="sxs-lookup"><span data-stu-id="2f1ba-140">Continue</span></span>
- <span data-ttu-id="2f1ba-141">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="2f1ba-141">Ignore</span></span>
- <span data-ttu-id="2f1ba-142">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="2f1ba-142">Inquire</span></span>
- <span data-ttu-id="2f1ba-143">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2f1ba-143">SilentlyContinue</span></span>
- <span data-ttu-id="2f1ba-144">Остановить</span><span class="sxs-lookup"><span data-stu-id="2f1ba-144">Stop</span></span>
- <span data-ttu-id="2f1ba-145">Рвать</span><span class="sxs-lookup"><span data-stu-id="2f1ba-145">Suspend</span></span>

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

### <span data-ttu-id="2f1ba-146">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2f1ba-146">-InformationVariable</span></span>
<span data-ttu-id="2f1ba-147">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-147">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2f1ba-148">-Location</span><span class="sxs-lookup"><span data-stu-id="2f1ba-148">-Location</span></span>
<span data-ttu-id="2f1ba-149">Расположение удостоверения ресурса для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-149">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="2f1ba-150">Это необходимо, если используется параметр-AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-150">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="2f1ba-151">-Metadata</span><span class="sxs-lookup"><span data-stu-id="2f1ba-151">-Metadata</span></span>
<span data-ttu-id="2f1ba-152">Обновленные метаданные для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-152">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="2f1ba-153">Это может быть либо путь к имени файла, содержащему метаданные, либо метаданные в виде строки.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-153">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="2f1ba-154">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2f1ba-154">-Name</span></span>
<span data-ttu-id="2f1ba-155">Указывает имя назначения политики, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-155">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="2f1ba-156">-NotScope</span><span class="sxs-lookup"><span data-stu-id="2f1ba-156">-NotScope</span></span>
<span data-ttu-id="2f1ba-157">Назначение политики не является областью действия.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-157">The policy assignment not scopes.</span></span>

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

### <span data-ttu-id="2f1ba-158">-Pre</span><span class="sxs-lookup"><span data-stu-id="2f1ba-158">-Pre</span></span>
<span data-ttu-id="2f1ba-159">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-159">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="2f1ba-160">-Scope</span><span class="sxs-lookup"><span data-stu-id="2f1ba-160">-Scope</span></span>
<span data-ttu-id="2f1ba-161">Указывает область применения политики.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-161">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="2f1ba-162">-SKU</span><span class="sxs-lookup"><span data-stu-id="2f1ba-162">-Sku</span></span>
<span data-ttu-id="2f1ba-163">Хэш-таблица, представляющая свойства SKU.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-163">A hash table which represents sku properties.</span></span>

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

### <span data-ttu-id="2f1ba-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f1ba-164">CommonParameters</span></span>
<span data-ttu-id="2f1ba-165">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2f1ba-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f1ba-166">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f1ba-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f1ba-167">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2f1ba-167">INPUTS</span></span>

## <span data-ttu-id="2f1ba-168">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f1ba-168">OUTPUTS</span></span>

## <span data-ttu-id="2f1ba-169">Пуск</span><span class="sxs-lookup"><span data-stu-id="2f1ba-169">NOTES</span></span>

## <span data-ttu-id="2f1ba-170">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2f1ba-170">RELATED LINKS</span></span>

[<span data-ttu-id="2f1ba-171">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="2f1ba-171">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="2f1ba-172">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="2f1ba-172">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="2f1ba-173">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="2f1ba-173">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)


