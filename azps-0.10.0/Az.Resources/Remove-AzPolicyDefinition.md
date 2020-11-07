---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
ms.openlocfilehash: 8cd1ee1d8f32bd203e9fb2d8ac5d75c2d6b2938d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910849"
---
# <span data-ttu-id="8a8be-101">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8a8be-101">Remove-AzPolicyDefinition</span></span>

## <span data-ttu-id="8a8be-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8a8be-102">SYNOPSIS</span></span>
<span data-ttu-id="8a8be-103">Удаляет определение политики.</span><span class="sxs-lookup"><span data-stu-id="8a8be-103">Removes a policy definition.</span></span>

## <span data-ttu-id="8a8be-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8a8be-104">SYNTAX</span></span>

### <span data-ttu-id="8a8be-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8a8be-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a8be-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a8be-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -ManagementGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a8be-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a8be-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a8be-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a8be-108">IdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a8be-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a8be-109">DESCRIPTION</span></span>
<span data-ttu-id="8a8be-110">Командлет **Remove-AzPolicyDefinition** удаляет определение политики.</span><span class="sxs-lookup"><span data-stu-id="8a8be-110">The **Remove-AzPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="8a8be-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8a8be-111">EXAMPLES</span></span>

### <span data-ttu-id="8a8be-112">Пример 1: Удаление определения политики по имени</span><span class="sxs-lookup"><span data-stu-id="8a8be-112">Example 1: Remove the policy definition by name</span></span>
```
PS C:\> Remove-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="8a8be-113">Эта команда удаляет указанное определение политики.</span><span class="sxs-lookup"><span data-stu-id="8a8be-113">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="8a8be-114">Пример 2: Удаление определения политики по ИДЕНТИФИКАТОРу ресурса</span><span class="sxs-lookup"><span data-stu-id="8a8be-114">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition' 
PS C:\> Remove-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="8a8be-115">Первая команда получает определение политики с именем VMPolicyDefinition с помощью командлета Get-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="8a8be-115">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="8a8be-116">Команда сохраняет его в переменной $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="8a8be-116">The command stores it in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="8a8be-117">Вторая команда удаляет определение политики, определяемое свойством **ResourceId** $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="8a8be-117">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="8a8be-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8a8be-118">PARAMETERS</span></span>

### <span data-ttu-id="8a8be-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8a8be-119">-ApiVersion</span></span>
<span data-ttu-id="8a8be-120">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8a8be-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="8a8be-121">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="8a8be-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="8a8be-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a8be-122">-DefaultProfile</span></span>
<span data-ttu-id="8a8be-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8a8be-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8a8be-124">-Force</span><span class="sxs-lookup"><span data-stu-id="8a8be-124">-Force</span></span>
<span data-ttu-id="8a8be-125">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="8a8be-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8a8be-126">-ID</span><span class="sxs-lookup"><span data-stu-id="8a8be-126">-Id</span></span>
<span data-ttu-id="8a8be-127">Указывает полный идентификатор ресурса для определения политики, которое удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="8a8be-127">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8a8be-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8a8be-128">-InformationAction</span></span>
<span data-ttu-id="8a8be-129">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="8a8be-129">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="8a8be-130">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="8a8be-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8a8be-131">Продолжал</span><span class="sxs-lookup"><span data-stu-id="8a8be-131">Continue</span></span>
- <span data-ttu-id="8a8be-132">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="8a8be-132">Ignore</span></span>
- <span data-ttu-id="8a8be-133">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="8a8be-133">Inquire</span></span>
- <span data-ttu-id="8a8be-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8a8be-134">SilentlyContinue</span></span>
- <span data-ttu-id="8a8be-135">Остановить</span><span class="sxs-lookup"><span data-stu-id="8a8be-135">Stop</span></span>
- <span data-ttu-id="8a8be-136">Рвать</span><span class="sxs-lookup"><span data-stu-id="8a8be-136">Suspend</span></span>

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

### <span data-ttu-id="8a8be-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8a8be-137">-InformationVariable</span></span>
<span data-ttu-id="8a8be-138">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="8a8be-138">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8a8be-139">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="8a8be-139">-ManagementGroupName</span></span>
<span data-ttu-id="8a8be-140">Имя группы управления для определения политики, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="8a8be-140">The name of the management group of the policy definition to delete.</span></span>

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

### <span data-ttu-id="8a8be-141">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8a8be-141">-Name</span></span>
<span data-ttu-id="8a8be-142">Указывает имя определения политики, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="8a8be-142">Specifies the name of the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8a8be-143">-Pre</span><span class="sxs-lookup"><span data-stu-id="8a8be-143">-Pre</span></span>
<span data-ttu-id="8a8be-144">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="8a8be-144">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8a8be-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8a8be-145">-SubscriptionId</span></span>
<span data-ttu-id="8a8be-146">Идентификатор подписки определения политики, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="8a8be-146">The subscription ID of the policy definition to delete.</span></span>

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

### <span data-ttu-id="8a8be-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8a8be-147">-Confirm</span></span>
<span data-ttu-id="8a8be-148">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8a8be-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a8be-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a8be-149">-WhatIf</span></span>
<span data-ttu-id="8a8be-150">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8a8be-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a8be-151">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8a8be-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a8be-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a8be-152">CommonParameters</span></span>
<span data-ttu-id="8a8be-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8a8be-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a8be-154">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a8be-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a8be-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8a8be-155">INPUTS</span></span>

## <span data-ttu-id="8a8be-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a8be-156">OUTPUTS</span></span>

## <span data-ttu-id="8a8be-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="8a8be-157">NOTES</span></span>

## <span data-ttu-id="8a8be-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8a8be-158">RELATED LINKS</span></span>

[<span data-ttu-id="8a8be-159">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8a8be-159">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="8a8be-160">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8a8be-160">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="8a8be-161">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8a8be-161">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


