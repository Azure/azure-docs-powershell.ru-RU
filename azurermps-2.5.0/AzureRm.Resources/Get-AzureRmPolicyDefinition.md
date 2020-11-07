---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicydefinition
schema: 2.0.0
ms.openlocfilehash: 5bd650583a933ba8d7ea56762c918d386b630c6c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913987"
---
# <span data-ttu-id="efe1b-101">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="efe1b-101">Get-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="efe1b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="efe1b-102">SYNOPSIS</span></span>
<span data-ttu-id="efe1b-103">Получение определений политики.</span><span class="sxs-lookup"><span data-stu-id="efe1b-103">Gets policy definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="efe1b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="efe1b-104">SYNTAX</span></span>

### <span data-ttu-id="efe1b-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="efe1b-105">NameParameterSet (Default)</span></span>
```
Get-AzureRmPolicyDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="efe1b-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="efe1b-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzureRmPolicyDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="efe1b-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="efe1b-107">SubscriptionIdParameterSet</span></span>
```
Get-AzureRmPolicyDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="efe1b-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="efe1b-108">IdParameterSet</span></span>
```
Get-AzureRmPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="efe1b-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="efe1b-109">BuiltinFilterParameterSet</span></span>
```
Get-AzureRmPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="efe1b-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="efe1b-110">CustomFilterParameterSet</span></span>
```
Get-AzureRmPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="efe1b-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="efe1b-111">DESCRIPTION</span></span>
<span data-ttu-id="efe1b-112">Командлет **Get-AzureRmPolicyDefinition** получает коллекцию определений политик или определенное определение политики, определяемое именем или идентификатором.</span><span class="sxs-lookup"><span data-stu-id="efe1b-112">The **Get-AzureRmPolicyDefinition** cmdlet gets a collection of policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="efe1b-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="efe1b-113">EXAMPLES</span></span>

### <span data-ttu-id="efe1b-114">Пример 1: получение всех определений политик</span><span class="sxs-lookup"><span data-stu-id="efe1b-114">Example 1: Get all policy definitions</span></span>
```
PS C:\> Get-AzureRmPolicyDefinition
```

<span data-ttu-id="efe1b-115">Эта команда получает все определения политики.</span><span class="sxs-lookup"><span data-stu-id="efe1b-115">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="efe1b-116">Пример 2: получение определения политики из текущей подписки по имени</span><span class="sxs-lookup"><span data-stu-id="efe1b-116">Example 2: Get policy definition from current subscription by name</span></span>
```
PS C:\> Get-AzureRmPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="efe1b-117">Эта команда получает определение политики с именем VMPolicyDefinition из текущей подписки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="efe1b-117">This command gets the policy definition named VMPolicyDefinition from the current default subscription.</span></span>

### <span data-ttu-id="efe1b-118">Пример 3: получение определения политики из группы управления по имени</span><span class="sxs-lookup"><span data-stu-id="efe1b-118">Example 3: Get policy definition from management group by name</span></span>
```
PS C:\> Get-AzureRmPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName 'Dept42'
```

<span data-ttu-id="efe1b-119">Эта команда получает определение политики с именем VMPolicyDefinition из группы управления с именем Dept42.</span><span class="sxs-lookup"><span data-stu-id="efe1b-119">This command gets the policy definition named VMPolicyDefinition from the management group named Dept42.</span></span>

### <span data-ttu-id="efe1b-120">Пример 4: получение всех встроенных определений политик из подписки</span><span class="sxs-lookup"><span data-stu-id="efe1b-120">Example 4: Get all built-in policy definitions from subscription</span></span>
```
PS C:\> Get-AzureRmPolicyDefinition -SubscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca' -Builtin
```

<span data-ttu-id="efe1b-121">Эта команда получает все встроенные определения политик из подписки с ИДЕНТИФИКАТОРом 3bf44b72-c631-427a-b8c8-53e2595398ca.</span><span class="sxs-lookup"><span data-stu-id="efe1b-121">This command gets all built-in policy definitions from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

## <span data-ttu-id="efe1b-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="efe1b-122">PARAMETERS</span></span>

### <span data-ttu-id="efe1b-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="efe1b-123">-ApiVersion</span></span>
<span data-ttu-id="efe1b-124">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="efe1b-124">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="efe1b-125">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="efe1b-125">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="efe1b-126">-Builtin</span><span class="sxs-lookup"><span data-stu-id="efe1b-126">-Builtin</span></span>
<span data-ttu-id="efe1b-127">Ограничивает список результатов только встроенными определениями политик.</span><span class="sxs-lookup"><span data-stu-id="efe1b-127">Limits list of results to only built-in policy definitions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BuiltinFilterParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efe1b-128">-Custom</span><span class="sxs-lookup"><span data-stu-id="efe1b-128">-Custom</span></span>
<span data-ttu-id="efe1b-129">Ограничивает список результатов только пользовательскими определениями политик.</span><span class="sxs-lookup"><span data-stu-id="efe1b-129">Limits list of results to only custom policy definitions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CustomFilterParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efe1b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efe1b-130">-DefaultProfile</span></span>
<span data-ttu-id="efe1b-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="efe1b-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="efe1b-132">-ID</span><span class="sxs-lookup"><span data-stu-id="efe1b-132">-Id</span></span>
<span data-ttu-id="efe1b-133">Указывает полный идентификатор ресурса для определения политики, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="efe1b-133">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="efe1b-134">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="efe1b-134">-InformationAction</span></span>
<span data-ttu-id="efe1b-135">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="efe1b-135">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="efe1b-136">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="efe1b-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="efe1b-137">Продолжал</span><span class="sxs-lookup"><span data-stu-id="efe1b-137">Continue</span></span>
- <span data-ttu-id="efe1b-138">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="efe1b-138">Ignore</span></span>
- <span data-ttu-id="efe1b-139">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="efe1b-139">Inquire</span></span>
- <span data-ttu-id="efe1b-140">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="efe1b-140">SilentlyContinue</span></span>
- <span data-ttu-id="efe1b-141">Остановить</span><span class="sxs-lookup"><span data-stu-id="efe1b-141">Stop</span></span>
- <span data-ttu-id="efe1b-142">Рвать</span><span class="sxs-lookup"><span data-stu-id="efe1b-142">Suspend</span></span>

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

### <span data-ttu-id="efe1b-143">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="efe1b-143">-InformationVariable</span></span>
<span data-ttu-id="efe1b-144">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="efe1b-144">Specifies an information variable.</span></span>

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

### <span data-ttu-id="efe1b-145">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="efe1b-145">-ManagementGroupName</span></span>
<span data-ttu-id="efe1b-146">Имя группы управления для определений политик, которые требуется получить.</span><span class="sxs-lookup"><span data-stu-id="efe1b-146">The name of the management group of the policy definition(s) to get.</span></span>

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

```yaml
Type: System.String
Parameter Sets: BuiltinFilterParameterSet, CustomFilterParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efe1b-147">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="efe1b-147">-Name</span></span>
<span data-ttu-id="efe1b-148">Указывает имя определения политики, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="efe1b-148">Specifies the name of the policy definition that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efe1b-149">-Pre</span><span class="sxs-lookup"><span data-stu-id="efe1b-149">-Pre</span></span>
<span data-ttu-id="efe1b-150">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="efe1b-150">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="efe1b-151">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="efe1b-151">-SubscriptionId</span></span>
<span data-ttu-id="efe1b-152">Идентификатор подписки определений политик, которые требуется получить.</span><span class="sxs-lookup"><span data-stu-id="efe1b-152">The subscription ID of the policy definition(s) to get.</span></span>

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

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: BuiltinFilterParameterSet, CustomFilterParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efe1b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efe1b-153">CommonParameters</span></span>
<span data-ttu-id="efe1b-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="efe1b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efe1b-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efe1b-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efe1b-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="efe1b-156">INPUTS</span></span>

## <span data-ttu-id="efe1b-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="efe1b-157">OUTPUTS</span></span>

## <span data-ttu-id="efe1b-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="efe1b-158">NOTES</span></span>

## <span data-ttu-id="efe1b-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="efe1b-159">RELATED LINKS</span></span>

[<span data-ttu-id="efe1b-160">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="efe1b-160">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="efe1b-161">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="efe1b-161">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="efe1b-162">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="efe1b-162">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


