---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
ms.openlocfilehash: a65892efce36490d256c99935f6cbe8a96f5ff98
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988921"
---
# <span data-ttu-id="b8013-101">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b8013-101">Remove-AzPolicyDefinition</span></span>

## <span data-ttu-id="b8013-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8013-102">SYNOPSIS</span></span>
<span data-ttu-id="b8013-103">Удаляет определение политики.</span><span class="sxs-lookup"><span data-stu-id="b8013-103">Removes a policy definition.</span></span>

## <span data-ttu-id="b8013-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b8013-104">SYNTAX</span></span>

### <span data-ttu-id="b8013-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b8013-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8013-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8013-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8013-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8013-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8013-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8013-108">IdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8013-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8013-109">InputObjectParameterSet</span></span>
```
Remove-AzPolicyDefinition [-Force] -InputObject <PsPolicyDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8013-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8013-110">DESCRIPTION</span></span>
<span data-ttu-id="b8013-111">Для **удаления определения политики удаляется cmdlet Remove-AzPolicyDefinition.**</span><span class="sxs-lookup"><span data-stu-id="b8013-111">The **Remove-AzPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="b8013-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b8013-112">EXAMPLES</span></span>

### <span data-ttu-id="b8013-113">Пример 1. Удаление определения политики по имени</span><span class="sxs-lookup"><span data-stu-id="b8013-113">Example 1: Remove the policy definition by name</span></span>
```
PS C:\> Remove-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="b8013-114">Эта команда удаляет указанное определение политики.</span><span class="sxs-lookup"><span data-stu-id="b8013-114">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="b8013-115">Пример 2. Удаление определения политики по ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="b8013-115">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition' 
PS C:\> Remove-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="b8013-116">Первая команда получает определение политики VMPolicyDefinition с помощью Get-AzPolicyDefinition командлета.</span><span class="sxs-lookup"><span data-stu-id="b8013-116">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="b8013-117">Команда сохраняет ее в переменной $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="b8013-117">The command stores it in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="b8013-118">Вторая команда удаляет определение политики, заданное свойством **ResourceId** $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="b8013-118">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="b8013-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8013-119">PARAMETERS</span></span>

### <span data-ttu-id="b8013-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b8013-120">-ApiVersion</span></span>
<span data-ttu-id="b8013-121">Определяет версию API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b8013-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="b8013-122">Если не указать версию, этот cmdlet использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="b8013-122">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="b8013-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8013-123">-DefaultProfile</span></span>
<span data-ttu-id="b8013-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b8013-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b8013-125">-Force</span><span class="sxs-lookup"><span data-stu-id="b8013-125">-Force</span></span>
<span data-ttu-id="b8013-126">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="b8013-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b8013-127">-Id</span><span class="sxs-lookup"><span data-stu-id="b8013-127">-Id</span></span>
<span data-ttu-id="b8013-128">Определяет полностью определенный код ресурса для определения политики, которое удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8013-128">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b8013-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8013-129">-InputObject</span></span>
<span data-ttu-id="b8013-130">Объект определения политики, который удаляется из другого cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8013-130">The policy definition object to remove that was output from another cmdlet.</span></span>

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

### <span data-ttu-id="b8013-131">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="b8013-131">-ManagementGroupName</span></span>
<span data-ttu-id="b8013-132">Имя группы управления в определении политики, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="b8013-132">The name of the management group of the policy definition to delete.</span></span>

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

### <span data-ttu-id="b8013-133">-Name</span><span class="sxs-lookup"><span data-stu-id="b8013-133">-Name</span></span>
<span data-ttu-id="b8013-134">Указывает имя определения политики, которое удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8013-134">Specifies the name of the policy definition that this cmdlet removes.</span></span>

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

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8013-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="b8013-135">-Pre</span></span>
<span data-ttu-id="b8013-136">Указывает на то, что этот cmdlet рассматривает предварительные версии API при автоматическом определении используемой версии.</span><span class="sxs-lookup"><span data-stu-id="b8013-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b8013-137">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b8013-137">-SubscriptionId</span></span>
<span data-ttu-id="b8013-138">ИД подписки, который нужно удалить в определении политики.</span><span class="sxs-lookup"><span data-stu-id="b8013-138">The subscription ID of the policy definition to delete.</span></span>

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

### <span data-ttu-id="b8013-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8013-139">-Confirm</span></span>
<span data-ttu-id="b8013-140">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8013-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8013-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8013-141">-WhatIf</span></span>
<span data-ttu-id="b8013-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8013-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8013-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b8013-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8013-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8013-144">CommonParameters</span></span>
<span data-ttu-id="b8013-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8013-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8013-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b8013-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8013-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b8013-147">INPUTS</span></span>

### <span data-ttu-id="b8013-148">System.String</span><span class="sxs-lookup"><span data-stu-id="b8013-148">System.String</span></span>

### <span data-ttu-id="b8013-149">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b8013-149">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="b8013-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b8013-150">OUTPUTS</span></span>

### <span data-ttu-id="b8013-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b8013-151">System.Boolean</span></span>

## <span data-ttu-id="b8013-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b8013-152">NOTES</span></span>

## <span data-ttu-id="b8013-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b8013-153">RELATED LINKS</span></span>

[<span data-ttu-id="b8013-154">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b8013-154">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="b8013-155">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b8013-155">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="b8013-156">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b8013-156">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


