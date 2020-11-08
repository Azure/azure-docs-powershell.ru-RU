---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
ms.openlocfilehash: c7d292a983090d8be22e159fbca6e423778b21f6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235418"
---
# <span data-ttu-id="52463-101">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="52463-101">Remove-AzPolicyDefinition</span></span>

## <span data-ttu-id="52463-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="52463-102">SYNOPSIS</span></span>
<span data-ttu-id="52463-103">Удаляет определение политики.</span><span class="sxs-lookup"><span data-stu-id="52463-103">Removes a policy definition.</span></span>

## <span data-ttu-id="52463-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="52463-104">SYNTAX</span></span>

### <span data-ttu-id="52463-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="52463-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52463-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="52463-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52463-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="52463-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52463-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="52463-108">IdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52463-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="52463-109">InputObjectParameterSet</span></span>
```
Remove-AzPolicyDefinition [-Force] -InputObject <PsPolicyDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52463-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="52463-110">DESCRIPTION</span></span>
<span data-ttu-id="52463-111">Командлет **Remove-AzPolicyDefinition** удаляет определение политики.</span><span class="sxs-lookup"><span data-stu-id="52463-111">The **Remove-AzPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="52463-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="52463-112">EXAMPLES</span></span>

### <span data-ttu-id="52463-113">Пример 1: Удаление определения политики по имени</span><span class="sxs-lookup"><span data-stu-id="52463-113">Example 1: Remove the policy definition by name</span></span>
```
PS C:\> Remove-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="52463-114">Эта команда удаляет указанное определение политики.</span><span class="sxs-lookup"><span data-stu-id="52463-114">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="52463-115">Пример 2: Удаление определения политики по ИДЕНТИФИКАТОРу ресурса</span><span class="sxs-lookup"><span data-stu-id="52463-115">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition' 
PS C:\> Remove-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="52463-116">Первая команда получает определение политики с именем VMPolicyDefinition с помощью командлета Get-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="52463-116">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="52463-117">Команда сохраняет его в переменной $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="52463-117">The command stores it in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="52463-118">Вторая команда удаляет определение политики, определяемое свойством **ResourceId** $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="52463-118">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="52463-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="52463-119">PARAMETERS</span></span>

### <span data-ttu-id="52463-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="52463-120">-ApiVersion</span></span>
<span data-ttu-id="52463-121">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="52463-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="52463-122">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="52463-122">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="52463-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52463-123">-DefaultProfile</span></span>
<span data-ttu-id="52463-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="52463-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="52463-125">-Force</span><span class="sxs-lookup"><span data-stu-id="52463-125">-Force</span></span>
<span data-ttu-id="52463-126">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="52463-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="52463-127">-ID</span><span class="sxs-lookup"><span data-stu-id="52463-127">-Id</span></span>
<span data-ttu-id="52463-128">Указывает полный идентификатор ресурса для определения политики, которое удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="52463-128">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="52463-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52463-129">-InputObject</span></span>
<span data-ttu-id="52463-130">Объект определения политики, который должен быть использован для удаления вывода из другого командлета.</span><span class="sxs-lookup"><span data-stu-id="52463-130">The policy definition object to remove that was output from another cmdlet.</span></span>

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

### <span data-ttu-id="52463-131">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="52463-131">-ManagementGroupName</span></span>
<span data-ttu-id="52463-132">Имя группы управления для определения политики, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="52463-132">The name of the management group of the policy definition to delete.</span></span>

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

### <span data-ttu-id="52463-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="52463-133">-Name</span></span>
<span data-ttu-id="52463-134">Указывает имя определения политики, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="52463-134">Specifies the name of the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="52463-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="52463-135">-Pre</span></span>
<span data-ttu-id="52463-136">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="52463-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="52463-137">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="52463-137">-SubscriptionId</span></span>
<span data-ttu-id="52463-138">Идентификатор подписки определения политики, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="52463-138">The subscription ID of the policy definition to delete.</span></span>

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

### <span data-ttu-id="52463-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="52463-139">-Confirm</span></span>
<span data-ttu-id="52463-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="52463-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52463-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52463-141">-WhatIf</span></span>
<span data-ttu-id="52463-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="52463-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52463-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="52463-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52463-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52463-144">CommonParameters</span></span>
<span data-ttu-id="52463-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="52463-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52463-146">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52463-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52463-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="52463-147">INPUTS</span></span>

### <span data-ttu-id="52463-148">System. String</span><span class="sxs-lookup"><span data-stu-id="52463-148">System.String</span></span>

### <span data-ttu-id="52463-149">System. Nullable "1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="52463-149">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="52463-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="52463-150">OUTPUTS</span></span>

### <span data-ttu-id="52463-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="52463-151">System.Boolean</span></span>

## <span data-ttu-id="52463-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="52463-152">NOTES</span></span>

## <span data-ttu-id="52463-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="52463-153">RELATED LINKS</span></span>

[<span data-ttu-id="52463-154">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="52463-154">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="52463-155">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="52463-155">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="52463-156">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="52463-156">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


