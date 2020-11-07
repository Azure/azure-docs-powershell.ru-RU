---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
ms.openlocfilehash: d0a1097407c9941b5be49b19ea7ba99e75b3fce2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734123"
---
# <span data-ttu-id="fc5b0-101">Get-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="fc5b0-101">Get-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="fc5b0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fc5b0-102">SYNOPSIS</span></span>
<span data-ttu-id="fc5b0-103">Получение определений политики.</span><span class="sxs-lookup"><span data-stu-id="fc5b0-103">Gets policy set definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc5b0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fc5b0-104">SYNTAX</span></span>

### <span data-ttu-id="fc5b0-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fc5b0-105">NameParameterSet (Default)</span></span>
```
Get-AzureRmPolicySetDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc5b0-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc5b0-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzureRmPolicySetDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc5b0-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc5b0-107">SubscriptionIdParameterSet</span></span>
```
Get-AzureRmPolicySetDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc5b0-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc5b0-108">IdParameterSet</span></span>
```
Get-AzureRmPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc5b0-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc5b0-109">BuiltinFilterParameterSet</span></span>
```
Get-AzureRmPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc5b0-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc5b0-110">CustomFilterParameterSet</span></span>
```
Get-AzureRmPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc5b0-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc5b0-111">DESCRIPTION</span></span>
<span data-ttu-id="fc5b0-112">Командлет **Get-AzureRmPolicySetDefinition** получает коллекцию определений политик или определенную определенную политику, определяемую именем или идентификатором.</span><span class="sxs-lookup"><span data-stu-id="fc5b0-112">The **Get-AzureRmPolicySetDefinition** cmdlet gets a collection of policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="fc5b0-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fc5b0-113">EXAMPLES</span></span>

### <span data-ttu-id="fc5b0-114">Пример 1: получение определений всех наборов политик</span><span class="sxs-lookup"><span data-stu-id="fc5b0-114">Example 1: Get all policy set definitions</span></span>
```
PS C:\> Get-AzureRmPolicySetDefinition
```

<span data-ttu-id="fc5b0-115">Эта команда получает все определения политики.</span><span class="sxs-lookup"><span data-stu-id="fc5b0-115">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="fc5b0-116">Пример 2: получение определения политики из текущей подписки по имени</span><span class="sxs-lookup"><span data-stu-id="fc5b0-116">Example 2: Get policy set definition from current subscription by name</span></span>
```
PS C:\> Get-AzureRmPolicySetDefinition -Name 'VMPolicySetDefinition'
```

<span data-ttu-id="fc5b0-117">Эта команда получает определение политики с именем VMPolicySetDefinition из текущей подписки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fc5b0-117">This command gets the policy set definition named VMPolicySetDefinition from the current default subscription.</span></span>

### <span data-ttu-id="fc5b0-118">Пример 3: получение определения политики из подписки по имени</span><span class="sxs-lookup"><span data-stu-id="fc5b0-118">Example 3: Get policy set definition from subscription by name</span></span>
```
PS C:\> Get-AzureRmPolicySetDefinition -Name 'VMPolicySetDefinition' -subscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca'
```

<span data-ttu-id="fc5b0-119">Эта команда получает определение политики с именем VMPolicySetDefinition из подписки с ИДЕНТИФИКАТОРом 3bf44b72-c631-427a-b8c8-53e2595398ca.</span><span class="sxs-lookup"><span data-stu-id="fc5b0-119">This command gets the policy definition named VMPolicySetDefinition from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

### <span data-ttu-id="fc5b0-120">Пример 4: получение всех настраиваемых определений политики из группы управления</span><span class="sxs-lookup"><span data-stu-id="fc5b0-120">Example 4: Get all custom policy set definitions from management group</span></span>
```
PS C:\> Get-AzureRmPolicySetDefinition -ManagementGroupName 'Dept42' -Custom
```

<span data-ttu-id="fc5b0-121">Эта команда получает определения всех настраиваемых наборов политик из группы управления с именем Dept42.</span><span class="sxs-lookup"><span data-stu-id="fc5b0-121">This command gets all custom policy set definitions from the management group named Dept42.</span></span>

## <span data-ttu-id="fc5b0-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fc5b0-122">PARAMETERS</span></span>

### <span data-ttu-id="fc5b0-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="fc5b0-123">-ApiVersion</span></span>
<span data-ttu-id="fc5b0-124">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fc5b0-124">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="fc5b0-125">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="fc5b0-125">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="fc5b0-126">-Builtin</span><span class="sxs-lookup"><span data-stu-id="fc5b0-126">-Builtin</span></span>
<span data-ttu-id="fc5b0-127">Ограничивает список результатов только встроенными определениями политик.</span><span class="sxs-lookup"><span data-stu-id="fc5b0-127">Limits list of results to only built-in policy set definitions.</span></span>

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

### <span data-ttu-id="fc5b0-128">-Custom</span><span class="sxs-lookup"><span data-stu-id="fc5b0-128">-Custom</span></span>
<span data-ttu-id="fc5b0-129">Ограничивает список результатов только настраиваемыми определениями политик.</span><span class="sxs-lookup"><span data-stu-id="fc5b0-129">Limits list of results to only custom policy set definitions.</span></span>

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

### <span data-ttu-id="fc5b0-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc5b0-130">-DefaultProfile</span></span>
<span data-ttu-id="fc5b0-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="fc5b0-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc5b0-132">-ID</span><span class="sxs-lookup"><span data-stu-id="fc5b0-132">-Id</span></span>
<span data-ttu-id="fc5b0-133">Полный идентификатор определения политики, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="fc5b0-133">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="fc5b0-134">Например,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="fc5b0-134">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="fc5b0-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="fc5b0-135">-ManagementGroupName</span></span>
<span data-ttu-id="fc5b0-136">Имя группы управления для определения политики, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="fc5b0-136">The name of the management group of the policy set definition(s) to get.</span></span>

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

### <span data-ttu-id="fc5b0-137">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fc5b0-137">-Name</span></span>
<span data-ttu-id="fc5b0-138">Имя определения настройки политики.</span><span class="sxs-lookup"><span data-stu-id="fc5b0-138">The policy set definition name.</span></span>

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

### <span data-ttu-id="fc5b0-139">-Pre</span><span class="sxs-lookup"><span data-stu-id="fc5b0-139">-Pre</span></span>
<span data-ttu-id="fc5b0-140">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="fc5b0-140">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="fc5b0-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fc5b0-141">-SubscriptionId</span></span>
<span data-ttu-id="fc5b0-142">Идентификатор подписки определений политики, которые требуется получить.</span><span class="sxs-lookup"><span data-stu-id="fc5b0-142">The subscription ID of the policy set definition(s) to get.</span></span>

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

### <span data-ttu-id="fc5b0-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc5b0-143">CommonParameters</span></span>
<span data-ttu-id="fc5b0-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fc5b0-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc5b0-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc5b0-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc5b0-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fc5b0-146">INPUTS</span></span>

### <span data-ttu-id="fc5b0-147">System. String</span><span class="sxs-lookup"><span data-stu-id="fc5b0-147">System.String</span></span>

### <span data-ttu-id="fc5b0-148">System. Nullable "1 [[System. GUID, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="fc5b0-148">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="fc5b0-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc5b0-149">OUTPUTS</span></span>

### <span data-ttu-id="fc5b0-150">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="fc5b0-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="fc5b0-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="fc5b0-151">NOTES</span></span>

## <span data-ttu-id="fc5b0-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fc5b0-152">RELATED LINKS</span></span>
