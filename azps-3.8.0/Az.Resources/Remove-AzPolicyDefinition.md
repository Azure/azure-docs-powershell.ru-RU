---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
ms.openlocfilehash: bd374f19a282ccafc3201a2965c33d4e8a3007ab
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066230"
---
# <span data-ttu-id="5b0a5-101">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5b0a5-101">Remove-AzPolicyDefinition</span></span>

## <span data-ttu-id="5b0a5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5b0a5-102">SYNOPSIS</span></span>
<span data-ttu-id="5b0a5-103">Удаляет определение политики.</span><span class="sxs-lookup"><span data-stu-id="5b0a5-103">Removes a policy definition.</span></span>

## <span data-ttu-id="5b0a5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5b0a5-104">SYNTAX</span></span>

### <span data-ttu-id="5b0a5-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5b0a5-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b0a5-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b0a5-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b0a5-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b0a5-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b0a5-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b0a5-108">IdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b0a5-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b0a5-109">DESCRIPTION</span></span>
<span data-ttu-id="5b0a5-110">Командлет **Remove-AzPolicyDefinition** удаляет определение политики.</span><span class="sxs-lookup"><span data-stu-id="5b0a5-110">The **Remove-AzPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="5b0a5-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5b0a5-111">EXAMPLES</span></span>

### <span data-ttu-id="5b0a5-112">Пример 1: Удаление определения политики по имени</span><span class="sxs-lookup"><span data-stu-id="5b0a5-112">Example 1: Remove the policy definition by name</span></span>
```
PS C:\> Remove-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="5b0a5-113">Эта команда удаляет указанное определение политики.</span><span class="sxs-lookup"><span data-stu-id="5b0a5-113">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="5b0a5-114">Пример 2: Удаление определения политики по ИДЕНТИФИКАТОРу ресурса</span><span class="sxs-lookup"><span data-stu-id="5b0a5-114">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition' 
PS C:\> Remove-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="5b0a5-115">Первая команда получает определение политики с именем VMPolicyDefinition с помощью командлета Get-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="5b0a5-115">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="5b0a5-116">Команда сохраняет его в переменной $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="5b0a5-116">The command stores it in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="5b0a5-117">Вторая команда удаляет определение политики, определяемое свойством **ResourceId** $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="5b0a5-117">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="5b0a5-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5b0a5-118">PARAMETERS</span></span>

### <span data-ttu-id="5b0a5-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5b0a5-119">-ApiVersion</span></span>
<span data-ttu-id="5b0a5-120">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5b0a5-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="5b0a5-121">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="5b0a5-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="5b0a5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b0a5-122">-DefaultProfile</span></span>
<span data-ttu-id="5b0a5-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5b0a5-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5b0a5-124">-Force</span><span class="sxs-lookup"><span data-stu-id="5b0a5-124">-Force</span></span>
<span data-ttu-id="5b0a5-125">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="5b0a5-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5b0a5-126">-ID</span><span class="sxs-lookup"><span data-stu-id="5b0a5-126">-Id</span></span>
<span data-ttu-id="5b0a5-127">Указывает полный идентификатор ресурса для определения политики, которое удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="5b0a5-127">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5b0a5-128">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="5b0a5-128">-ManagementGroupName</span></span>
<span data-ttu-id="5b0a5-129">Имя группы управления для определения политики, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="5b0a5-129">The name of the management group of the policy definition to delete.</span></span>

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

### <span data-ttu-id="5b0a5-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5b0a5-130">-Name</span></span>
<span data-ttu-id="5b0a5-131">Указывает имя определения политики, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5b0a5-131">Specifies the name of the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5b0a5-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="5b0a5-132">-Pre</span></span>
<span data-ttu-id="5b0a5-133">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="5b0a5-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="5b0a5-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5b0a5-134">-SubscriptionId</span></span>
<span data-ttu-id="5b0a5-135">Идентификатор подписки определения политики, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="5b0a5-135">The subscription ID of the policy definition to delete.</span></span>

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

### <span data-ttu-id="5b0a5-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5b0a5-136">-Confirm</span></span>
<span data-ttu-id="5b0a5-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5b0a5-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b0a5-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b0a5-138">-WhatIf</span></span>
<span data-ttu-id="5b0a5-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5b0a5-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b0a5-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5b0a5-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b0a5-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b0a5-141">CommonParameters</span></span>
<span data-ttu-id="5b0a5-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5b0a5-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b0a5-143">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5b0a5-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b0a5-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5b0a5-144">INPUTS</span></span>

### <span data-ttu-id="5b0a5-145">System. String</span><span class="sxs-lookup"><span data-stu-id="5b0a5-145">System.String</span></span>

### <span data-ttu-id="5b0a5-146">System. Nullable "1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5b0a5-146">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="5b0a5-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b0a5-147">OUTPUTS</span></span>

### <span data-ttu-id="5b0a5-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5b0a5-148">System.Boolean</span></span>

## <span data-ttu-id="5b0a5-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="5b0a5-149">NOTES</span></span>

## <span data-ttu-id="5b0a5-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5b0a5-150">RELATED LINKS</span></span>

[<span data-ttu-id="5b0a5-151">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5b0a5-151">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="5b0a5-152">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5b0a5-152">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="5b0a5-153">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5b0a5-153">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


