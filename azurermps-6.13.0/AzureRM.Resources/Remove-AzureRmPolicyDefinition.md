---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
ms.openlocfilehash: 9d59a974a29743004228efb414a92627782bd8e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733805"
---
# <span data-ttu-id="30aa9-101">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="30aa9-101">Remove-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="30aa9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="30aa9-102">SYNOPSIS</span></span>
<span data-ttu-id="30aa9-103">Удаляет определение политики.</span><span class="sxs-lookup"><span data-stu-id="30aa9-103">Removes a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30aa9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="30aa9-104">SYNTAX</span></span>

### <span data-ttu-id="30aa9-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="30aa9-105">NameParameterSet (Default)</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30aa9-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="30aa9-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] -ManagementGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30aa9-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="30aa9-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30aa9-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="30aa9-108">IdParameterSet</span></span>
```
Remove-AzureRmPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30aa9-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="30aa9-109">DESCRIPTION</span></span>
<span data-ttu-id="30aa9-110">Командлет **Remove-AzureRmPolicyDefinition** удаляет определение политики.</span><span class="sxs-lookup"><span data-stu-id="30aa9-110">The **Remove-AzureRmPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="30aa9-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="30aa9-111">EXAMPLES</span></span>

### <span data-ttu-id="30aa9-112">Пример 1: Удаление определения политики по имени</span><span class="sxs-lookup"><span data-stu-id="30aa9-112">Example 1: Remove the policy definition by name</span></span>
```
PS C:\> Remove-AzureRmPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="30aa9-113">Эта команда удаляет указанное определение политики.</span><span class="sxs-lookup"><span data-stu-id="30aa9-113">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="30aa9-114">Пример 2: Удаление определения политики по ИДЕНТИФИКАТОРу ресурса</span><span class="sxs-lookup"><span data-stu-id="30aa9-114">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\> $PolicyDefinition = Get-AzureRmPolicyDefinition -Name 'VMPolicyDefinition' 
PS C:\> Remove-AzureRmPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="30aa9-115">Первая команда получает определение политики с именем VMPolicyDefinition с помощью командлета Get-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="30aa9-115">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="30aa9-116">Команда сохраняет его в переменной $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="30aa9-116">The command stores it in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="30aa9-117">Вторая команда удаляет определение политики, определяемое свойством **ResourceId** $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="30aa9-117">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="30aa9-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="30aa9-118">PARAMETERS</span></span>

### <span data-ttu-id="30aa9-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="30aa9-119">-ApiVersion</span></span>
<span data-ttu-id="30aa9-120">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="30aa9-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="30aa9-121">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="30aa9-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="30aa9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30aa9-122">-DefaultProfile</span></span>
<span data-ttu-id="30aa9-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="30aa9-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30aa9-124">-Force</span><span class="sxs-lookup"><span data-stu-id="30aa9-124">-Force</span></span>
<span data-ttu-id="30aa9-125">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="30aa9-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="30aa9-126">-ID</span><span class="sxs-lookup"><span data-stu-id="30aa9-126">-Id</span></span>
<span data-ttu-id="30aa9-127">Указывает полный идентификатор ресурса для определения политики, которое удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="30aa9-127">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="30aa9-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="30aa9-128">-InformationAction</span></span>
<span data-ttu-id="30aa9-129">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="30aa9-129">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="30aa9-130">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="30aa9-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="30aa9-131">Продолжал</span><span class="sxs-lookup"><span data-stu-id="30aa9-131">Continue</span></span>
- <span data-ttu-id="30aa9-132">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="30aa9-132">Ignore</span></span>
- <span data-ttu-id="30aa9-133">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="30aa9-133">Inquire</span></span>
- <span data-ttu-id="30aa9-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="30aa9-134">SilentlyContinue</span></span>
- <span data-ttu-id="30aa9-135">Остановить</span><span class="sxs-lookup"><span data-stu-id="30aa9-135">Stop</span></span>
- <span data-ttu-id="30aa9-136">Рвать</span><span class="sxs-lookup"><span data-stu-id="30aa9-136">Suspend</span></span>

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

### <span data-ttu-id="30aa9-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="30aa9-137">-InformationVariable</span></span>
<span data-ttu-id="30aa9-138">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="30aa9-138">Specifies an information variable.</span></span>

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

### <span data-ttu-id="30aa9-139">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="30aa9-139">-ManagementGroupName</span></span>
<span data-ttu-id="30aa9-140">Имя группы управления для определения политики, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="30aa9-140">The name of the management group of the policy definition to delete.</span></span>

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

### <span data-ttu-id="30aa9-141">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="30aa9-141">-Name</span></span>
<span data-ttu-id="30aa9-142">Указывает имя определения политики, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="30aa9-142">Specifies the name of the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="30aa9-143">-Pre</span><span class="sxs-lookup"><span data-stu-id="30aa9-143">-Pre</span></span>
<span data-ttu-id="30aa9-144">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="30aa9-144">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="30aa9-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="30aa9-145">-SubscriptionId</span></span>
<span data-ttu-id="30aa9-146">Идентификатор подписки определения политики, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="30aa9-146">The subscription ID of the policy definition to delete.</span></span>

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

### <span data-ttu-id="30aa9-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="30aa9-147">-Confirm</span></span>
<span data-ttu-id="30aa9-148">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="30aa9-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30aa9-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30aa9-149">-WhatIf</span></span>
<span data-ttu-id="30aa9-150">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="30aa9-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30aa9-151">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="30aa9-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30aa9-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30aa9-152">CommonParameters</span></span>
<span data-ttu-id="30aa9-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="30aa9-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30aa9-154">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30aa9-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30aa9-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="30aa9-155">INPUTS</span></span>

## <span data-ttu-id="30aa9-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="30aa9-156">OUTPUTS</span></span>

## <span data-ttu-id="30aa9-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="30aa9-157">NOTES</span></span>

## <span data-ttu-id="30aa9-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="30aa9-158">RELATED LINKS</span></span>

[<span data-ttu-id="30aa9-159">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="30aa9-159">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="30aa9-160">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="30aa9-160">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="30aa9-161">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="30aa9-161">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


