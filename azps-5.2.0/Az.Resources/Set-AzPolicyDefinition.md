---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
ms.openlocfilehash: 3aed403965bc48a26044b930fdf5cc9e9a93bbbe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405607"
---
# <span data-ttu-id="7d042-101">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7d042-101">Set-AzPolicyDefinition</span></span>

## <span data-ttu-id="7d042-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d042-102">SYNOPSIS</span></span>
<span data-ttu-id="7d042-103">Изменяет определение политики.</span><span class="sxs-lookup"><span data-stu-id="7d042-103">Modifies a policy definition.</span></span>

## <span data-ttu-id="7d042-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7d042-104">SYNTAX</span></span>

### <span data-ttu-id="7d042-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7d042-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d042-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d042-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d042-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d042-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d042-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d042-108">IdParameterSet</span></span>
```
Set-AzPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d042-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d042-109">InputObjectParameterSet</span></span>
```
Set-AzPolicyDefinition [-DisplayName <String>] [-Description <String>] [-Policy <String>] [-Metadata <String>]
 [-Parameter <String>] [-Mode <String>] -InputObject <PsPolicyDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d042-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d042-110">DESCRIPTION</span></span>
<span data-ttu-id="7d042-111">При этом определение политики **изменяется** с его наличием.</span><span class="sxs-lookup"><span data-stu-id="7d042-111">The **Set-AzPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="7d042-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7d042-112">EXAMPLES</span></span>

### <span data-ttu-id="7d042-113">Пример 1. Обновление описания определения политики</span><span class="sxs-lookup"><span data-stu-id="7d042-113">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="7d042-114">Первая команда получает определение политики VMPolicyDefinition с помощью Get-AzPolicyDefinition командлета.</span><span class="sxs-lookup"><span data-stu-id="7d042-114">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="7d042-115">Эта команда сохраняет этот объект в $PolicyDefinition переменной.</span><span class="sxs-lookup"><span data-stu-id="7d042-115">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="7d042-116">Вторая команда обновляет описание определения политики, заданного **свойством ResourceId** $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="7d042-116">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="7d042-117">Пример 2. Обновление режима определения политики</span><span class="sxs-lookup"><span data-stu-id="7d042-117">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="7d042-118">Эта команда обновляет определение политики VMPolicyDefinition, используя Set-AzPolicyDefinition для свойства режима "Все".</span><span class="sxs-lookup"><span data-stu-id="7d042-118">This command updates the policy definition named VMPolicyDefinition by using the Set-AzPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

### <span data-ttu-id="7d042-119">Пример 3. Обновление метаданных определения политики</span><span class="sxs-lookup"><span data-stu-id="7d042-119">Example 3: Update the metadata of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Metadata '{"category":"Virtual Machine"}'


Name               : VMPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
ResourceName       : VMPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=VMPolicyDefinition; policyType=Custom; mode=All; metadata=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
```

<span data-ttu-id="7d042-120">Эта команда обновляет метаданные определения политики VMPolicyDefinition, чтобы указать для категории виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="7d042-120">This command updates the metadata of a policy definition named VMPolicyDefinition to indicate its category is "Virtual Machine".</span></span>

## <span data-ttu-id="7d042-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d042-121">PARAMETERS</span></span>

### <span data-ttu-id="7d042-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7d042-122">-ApiVersion</span></span>
<span data-ttu-id="7d042-123">Определяет версию API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7d042-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="7d042-124">Если не указать версию, этот cmdlet использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="7d042-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="7d042-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d042-125">-DefaultProfile</span></span>
<span data-ttu-id="7d042-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7d042-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d042-127">-Description</span><span class="sxs-lookup"><span data-stu-id="7d042-127">-Description</span></span>
<span data-ttu-id="7d042-128">Указывает новое описание определения политики.</span><span class="sxs-lookup"><span data-stu-id="7d042-128">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="7d042-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7d042-129">-DisplayName</span></span>
<span data-ttu-id="7d042-130">Указывает новое отображаемого имя для определения политики.</span><span class="sxs-lookup"><span data-stu-id="7d042-130">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="7d042-131">-Id</span><span class="sxs-lookup"><span data-stu-id="7d042-131">-Id</span></span>
<span data-ttu-id="7d042-132">Определяет полностью определенный код ресурса для определения политики, которое изменяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d042-132">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="7d042-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d042-133">-InputObject</span></span>
<span data-ttu-id="7d042-134">Объект определения политики, обновляемого из другого cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d042-134">The policy definition object to update that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyDefinition
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d042-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="7d042-135">-ManagementGroupName</span></span>
<span data-ttu-id="7d042-136">Имя группы управления обновляемого определения политики.</span><span class="sxs-lookup"><span data-stu-id="7d042-136">The name of the management group of the policy definition to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d042-137">-Метаданные</span><span class="sxs-lookup"><span data-stu-id="7d042-137">-Metadata</span></span>
<span data-ttu-id="7d042-138">Метаданные определения политики.</span><span class="sxs-lookup"><span data-stu-id="7d042-138">The metadata for policy definition.</span></span> <span data-ttu-id="7d042-139">Это может быть путь к имени файла, содержащего метаданные, или метаданные в виде строки.</span><span class="sxs-lookup"><span data-stu-id="7d042-139">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="7d042-140">-Mode</span><span class="sxs-lookup"><span data-stu-id="7d042-140">-Mode</span></span>
<span data-ttu-id="7d042-141">Режим нового определения политики.</span><span class="sxs-lookup"><span data-stu-id="7d042-141">The mode of the new policy definition.</span></span>

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

### <span data-ttu-id="7d042-142">-Name</span><span class="sxs-lookup"><span data-stu-id="7d042-142">-Name</span></span>
<span data-ttu-id="7d042-143">Указывает имя определения политики, которое изменяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d042-143">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d042-144">-Parameter</span><span class="sxs-lookup"><span data-stu-id="7d042-144">-Parameter</span></span>
<span data-ttu-id="7d042-145">Объявление параметров для определения политики.</span><span class="sxs-lookup"><span data-stu-id="7d042-145">The parameters declaration for policy definition.</span></span> <span data-ttu-id="7d042-146">Это может быть путь к имени файла или URI, содержащий объявление параметров, или объявление параметров в качестве строки.</span><span class="sxs-lookup"><span data-stu-id="7d042-146">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="7d042-147">-Политика</span><span class="sxs-lookup"><span data-stu-id="7d042-147">-Policy</span></span>
<span data-ttu-id="7d042-148">Определяет новое правило политики для определения политики.</span><span class="sxs-lookup"><span data-stu-id="7d042-148">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="7d042-149">Вы можете указать путь к JSON-файлу или строке, которая содержит политику в формате нотации объектов JavaScript (JSON).</span><span class="sxs-lookup"><span data-stu-id="7d042-149">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="7d042-150">-Pre</span><span class="sxs-lookup"><span data-stu-id="7d042-150">-Pre</span></span>
<span data-ttu-id="7d042-151">Указывает на то, что этот cmdlet рассматривает предварительные версии API при автоматическом определении используемой версии.</span><span class="sxs-lookup"><span data-stu-id="7d042-151">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="7d042-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7d042-152">-SubscriptionId</span></span>
<span data-ttu-id="7d042-153">ИД подписки определения политики, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="7d042-153">The subscription ID of the policy definition to update.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d042-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d042-154">CommonParameters</span></span>
<span data-ttu-id="7d042-155">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d042-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d042-156">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7d042-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d042-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7d042-157">INPUTS</span></span>

### <span data-ttu-id="7d042-158">System.String</span><span class="sxs-lookup"><span data-stu-id="7d042-158">System.String</span></span>

### <span data-ttu-id="7d042-159">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7d042-159">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="7d042-160">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7d042-160">OUTPUTS</span></span>

### <span data-ttu-id="7d042-161">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="7d042-161">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="7d042-162">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7d042-162">NOTES</span></span>

## <span data-ttu-id="7d042-163">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7d042-163">RELATED LINKS</span></span>

[<span data-ttu-id="7d042-164">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7d042-164">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="7d042-165">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7d042-165">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="7d042-166">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7d042-166">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)


