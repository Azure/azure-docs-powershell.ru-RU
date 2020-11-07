---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzPolicyDefinition.md
ms.openlocfilehash: 66901872a6a7c3e871ce95287b45966aee974b52
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910944"
---
# <span data-ttu-id="8a9b4-101">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8a9b4-101">Get-AzPolicyDefinition</span></span>

## <span data-ttu-id="8a9b4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8a9b4-102">SYNOPSIS</span></span>
<span data-ttu-id="8a9b4-103">Получение определений политики.</span><span class="sxs-lookup"><span data-stu-id="8a9b4-103">Gets policy definitions.</span></span>

## <span data-ttu-id="8a9b4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8a9b4-104">SYNTAX</span></span>

### <span data-ttu-id="8a9b4-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8a9b4-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicyDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8a9b4-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a9b4-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8a9b4-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a9b4-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8a9b4-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a9b4-108">IdParameterSet</span></span>
```
Get-AzPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8a9b4-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a9b4-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8a9b4-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a9b4-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8a9b4-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a9b4-111">DESCRIPTION</span></span>
<span data-ttu-id="8a9b4-112">Командлет **Get-AzPolicyDefinition** получает коллекцию определений политик или определенное определение политики, определяемое именем или идентификатором.</span><span class="sxs-lookup"><span data-stu-id="8a9b4-112">The **Get-AzPolicyDefinition** cmdlet gets a collection of policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="8a9b4-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8a9b4-113">EXAMPLES</span></span>

### <span data-ttu-id="8a9b4-114">Пример 1: получение всех определений политик</span><span class="sxs-lookup"><span data-stu-id="8a9b4-114">Example 1: Get all policy definitions</span></span>
```
PS C:\> Get-AzPolicyDefinition
```

<span data-ttu-id="8a9b4-115">Эта команда получает все определения политики.</span><span class="sxs-lookup"><span data-stu-id="8a9b4-115">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="8a9b4-116">Пример 2: получение определения политики из текущей подписки по имени</span><span class="sxs-lookup"><span data-stu-id="8a9b4-116">Example 2: Get policy definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="8a9b4-117">Эта команда получает определение политики с именем VMPolicyDefinition из текущей подписки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8a9b4-117">This command gets the policy definition named VMPolicyDefinition from the current default subscription.</span></span>

### <span data-ttu-id="8a9b4-118">Пример 3: получение определения политики из группы управления по имени</span><span class="sxs-lookup"><span data-stu-id="8a9b4-118">Example 3: Get policy definition from management group by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName 'Dept42'
```

<span data-ttu-id="8a9b4-119">Эта команда получает определение политики с именем VMPolicyDefinition из группы управления с именем Dept42.</span><span class="sxs-lookup"><span data-stu-id="8a9b4-119">This command gets the policy definition named VMPolicyDefinition from the management group named Dept42.</span></span>

### <span data-ttu-id="8a9b4-120">Пример 4: получение всех встроенных определений политик из подписки</span><span class="sxs-lookup"><span data-stu-id="8a9b4-120">Example 4: Get all built-in policy definitions from subscription</span></span>
```
PS C:\> Get-AzPolicyDefinition -SubscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca' -Builtin
```

<span data-ttu-id="8a9b4-121">Эта команда получает все встроенные определения политик из подписки с ИДЕНТИФИКАТОРом 3bf44b72-c631-427a-b8c8-53e2595398ca.</span><span class="sxs-lookup"><span data-stu-id="8a9b4-121">This command gets all built-in policy definitions from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

## <span data-ttu-id="8a9b4-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8a9b4-122">PARAMETERS</span></span>

### <span data-ttu-id="8a9b4-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8a9b4-123">-ApiVersion</span></span>
<span data-ttu-id="8a9b4-124">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8a9b4-124">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="8a9b4-125">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="8a9b4-125">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="8a9b4-126">-Builtin</span><span class="sxs-lookup"><span data-stu-id="8a9b4-126">-Builtin</span></span>
<span data-ttu-id="8a9b4-127">Ограничивает список результатов только встроенными определениями политик.</span><span class="sxs-lookup"><span data-stu-id="8a9b4-127">Limits list of results to only built-in policy definitions.</span></span>

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

### <span data-ttu-id="8a9b4-128">-Custom</span><span class="sxs-lookup"><span data-stu-id="8a9b4-128">-Custom</span></span>
<span data-ttu-id="8a9b4-129">Ограничивает список результатов только пользовательскими определениями политик.</span><span class="sxs-lookup"><span data-stu-id="8a9b4-129">Limits list of results to only custom policy definitions.</span></span>

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

### <span data-ttu-id="8a9b4-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a9b4-130">-DefaultProfile</span></span>
<span data-ttu-id="8a9b4-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8a9b4-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8a9b4-132">-ID</span><span class="sxs-lookup"><span data-stu-id="8a9b4-132">-Id</span></span>
<span data-ttu-id="8a9b4-133">Указывает полный идентификатор ресурса для определения политики, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="8a9b4-133">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8a9b4-134">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8a9b4-134">-InformationAction</span></span>
<span data-ttu-id="8a9b4-135">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="8a9b4-135">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="8a9b4-136">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="8a9b4-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8a9b4-137">Продолжал</span><span class="sxs-lookup"><span data-stu-id="8a9b4-137">Continue</span></span>
- <span data-ttu-id="8a9b4-138">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="8a9b4-138">Ignore</span></span>
- <span data-ttu-id="8a9b4-139">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="8a9b4-139">Inquire</span></span>
- <span data-ttu-id="8a9b4-140">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8a9b4-140">SilentlyContinue</span></span>
- <span data-ttu-id="8a9b4-141">Остановить</span><span class="sxs-lookup"><span data-stu-id="8a9b4-141">Stop</span></span>
- <span data-ttu-id="8a9b4-142">Рвать</span><span class="sxs-lookup"><span data-stu-id="8a9b4-142">Suspend</span></span>

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

### <span data-ttu-id="8a9b4-143">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8a9b4-143">-InformationVariable</span></span>
<span data-ttu-id="8a9b4-144">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="8a9b4-144">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8a9b4-145">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="8a9b4-145">-ManagementGroupName</span></span>
<span data-ttu-id="8a9b4-146">Имя группы управления для определений политик, которые требуется получить.</span><span class="sxs-lookup"><span data-stu-id="8a9b4-146">The name of the management group of the policy definition(s) to get.</span></span>

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

### <span data-ttu-id="8a9b4-147">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8a9b4-147">-Name</span></span>
<span data-ttu-id="8a9b4-148">Указывает имя определения политики, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="8a9b4-148">Specifies the name of the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8a9b4-149">-Pre</span><span class="sxs-lookup"><span data-stu-id="8a9b4-149">-Pre</span></span>
<span data-ttu-id="8a9b4-150">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="8a9b4-150">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8a9b4-151">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8a9b4-151">-SubscriptionId</span></span>
<span data-ttu-id="8a9b4-152">Идентификатор подписки определений политик, которые требуется получить.</span><span class="sxs-lookup"><span data-stu-id="8a9b4-152">The subscription ID of the policy definition(s) to get.</span></span>

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

### <span data-ttu-id="8a9b4-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a9b4-153">CommonParameters</span></span>
<span data-ttu-id="8a9b4-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8a9b4-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a9b4-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a9b4-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a9b4-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8a9b4-156">INPUTS</span></span>

## <span data-ttu-id="8a9b4-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a9b4-157">OUTPUTS</span></span>

## <span data-ttu-id="8a9b4-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="8a9b4-158">NOTES</span></span>

## <span data-ttu-id="8a9b4-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8a9b4-159">RELATED LINKS</span></span>

[<span data-ttu-id="8a9b4-160">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8a9b4-160">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="8a9b4-161">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8a9b4-161">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

[<span data-ttu-id="8a9b4-162">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8a9b4-162">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


