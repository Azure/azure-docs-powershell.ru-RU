---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/invoke-azurermresourceaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Invoke-AzureRmResourceAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Invoke-AzureRmResourceAction.md
ms.openlocfilehash: 0a8fa9f13e77617a7f9efbd31909edfd64bf353a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564031"
---
# <span data-ttu-id="32873-101">Invoke-AzureRmResourceAction</span><span class="sxs-lookup"><span data-stu-id="32873-101">Invoke-AzureRmResourceAction</span></span>

## <span data-ttu-id="32873-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="32873-102">SYNOPSIS</span></span>
<span data-ttu-id="32873-103">Вызывает действие с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="32873-103">Invokes an action on a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32873-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="32873-104">SYNTAX</span></span>

### <span data-ttu-id="32873-105">ByResourceId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="32873-105">ByResourceId (Default)</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String>
 [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="32873-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="32873-106">BySubscriptionLevel</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32873-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="32873-107">ByTenantLevel</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32873-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32873-108">DESCRIPTION</span></span>
<span data-ttu-id="32873-109">Командлет **Invoke-AzureRmResourceAction** вызывает действие с указанным ресурсом Azure.</span><span class="sxs-lookup"><span data-stu-id="32873-109">The **Invoke-AzureRmResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>
<span data-ttu-id="32873-110">Чтобы получить список поддерживаемых действий, воспользуйтесь средством "Обозреватель ресурсов Azure".</span><span class="sxs-lookup"><span data-stu-id="32873-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="32873-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="32873-111">EXAMPLES</span></span>

## <span data-ttu-id="32873-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="32873-112">PARAMETERS</span></span>

### <span data-ttu-id="32873-113">-Action (действие)</span><span class="sxs-lookup"><span data-stu-id="32873-113">-Action</span></span>
<span data-ttu-id="32873-114">Указывает имя вызываемого действия.</span><span class="sxs-lookup"><span data-stu-id="32873-114">Specifies the name of the action to invoke.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ActionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32873-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="32873-115">-ApiVersion</span></span>
<span data-ttu-id="32873-116">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="32873-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="32873-117">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="32873-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="32873-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32873-118">-DefaultProfile</span></span>
<span data-ttu-id="32873-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="32873-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32873-120">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="32873-120">-ExtensionResourceName</span></span>
<span data-ttu-id="32873-121">Указывает имя ресурса расширения для ресурса, в котором этот командлет вызывает действие.</span><span class="sxs-lookup"><span data-stu-id="32873-121">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="32873-122">Например, чтобы указать базу данных, используйте следующий формат: имя `/` базы данных имени сервера</span><span class="sxs-lookup"><span data-stu-id="32873-122">For instance, to specify a database, use the following format: server name`/`database name</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32873-123">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="32873-123">-ExtensionResourceType</span></span>
<span data-ttu-id="32873-124">Указывает тип ресурса расширения.</span><span class="sxs-lookup"><span data-stu-id="32873-124">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="32873-125">Например: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="32873-125">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32873-126">-Force</span><span class="sxs-lookup"><span data-stu-id="32873-126">-Force</span></span>
<span data-ttu-id="32873-127">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="32873-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="32873-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="32873-128">-InformationAction</span></span>
<span data-ttu-id="32873-129">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="32873-129">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="32873-130">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="32873-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="32873-131">Продолжал</span><span class="sxs-lookup"><span data-stu-id="32873-131">Continue</span></span>
- <span data-ttu-id="32873-132">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="32873-132">Ignore</span></span>
- <span data-ttu-id="32873-133">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="32873-133">Inquire</span></span>
- <span data-ttu-id="32873-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="32873-134">SilentlyContinue</span></span>
- <span data-ttu-id="32873-135">Остановить</span><span class="sxs-lookup"><span data-stu-id="32873-135">Stop</span></span>
- <span data-ttu-id="32873-136">Рвать</span><span class="sxs-lookup"><span data-stu-id="32873-136">Suspend</span></span>

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

### <span data-ttu-id="32873-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="32873-137">-InformationVariable</span></span>
<span data-ttu-id="32873-138">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="32873-138">Specifies an information variable.</span></span>

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

### <span data-ttu-id="32873-139">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="32873-139">-ODataQuery</span></span>
<span data-ttu-id="32873-140">Задает фильтр стиля Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="32873-140">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="32873-141">Этот командлет добавляет это значение в запрос в дополнение к любым другим фильтрам.</span><span class="sxs-lookup"><span data-stu-id="32873-141">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="32873-142">-Parameters</span><span class="sxs-lookup"><span data-stu-id="32873-142">-Parameters</span></span>
<span data-ttu-id="32873-143">Задает параметры, которые являются хэш-таблицами для действия, вызванного этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="32873-143">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Object

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32873-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="32873-144">-Pre</span></span>
<span data-ttu-id="32873-145">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="32873-145">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="32873-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32873-146">-ResourceGroupName</span></span>
<span data-ttu-id="32873-147">Указывает имя группы ресурсов, в которой этот командлет вызывает действие.</span><span class="sxs-lookup"><span data-stu-id="32873-147">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32873-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="32873-148">-ResourceId</span></span>
<span data-ttu-id="32873-149">Указывает полный ИД ресурса ресурса, в котором этот командлет вызывает действие.</span><span class="sxs-lookup"><span data-stu-id="32873-149">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="32873-150">Идентификатор включает подписку, как показано в следующем примере: `/subscriptions/` ИД подписки`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="32873-150">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32873-151">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="32873-151">-ResourceName</span></span>
<span data-ttu-id="32873-152">Указывает имя ресурса ресурса, который этот командлет вызывает действие.</span><span class="sxs-lookup"><span data-stu-id="32873-152">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="32873-153">Например, чтобы указать базу данных, используйте следующий формат: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="32873-153">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32873-154">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="32873-154">-ResourceType</span></span>
<span data-ttu-id="32873-155">Указывает тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="32873-155">Specifies the type of the resource.</span></span>
<span data-ttu-id="32873-156">Например, для базы данных тип ресурса выглядит следующим образом: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="32873-156">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32873-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="32873-157">-TenantLevel</span></span>
<span data-ttu-id="32873-158">Указывает на то, что этот командлет работает на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="32873-158">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32873-159">-Confirm</span><span class="sxs-lookup"><span data-stu-id="32873-159">-Confirm</span></span>
<span data-ttu-id="32873-160">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="32873-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32873-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32873-161">-WhatIf</span></span>
<span data-ttu-id="32873-162">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="32873-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32873-163">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="32873-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32873-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32873-164">CommonParameters</span></span>
<span data-ttu-id="32873-165">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="32873-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32873-166">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32873-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32873-167">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="32873-167">INPUTS</span></span>

## <span data-ttu-id="32873-168">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="32873-168">OUTPUTS</span></span>

## <span data-ttu-id="32873-169">Пуск</span><span class="sxs-lookup"><span data-stu-id="32873-169">NOTES</span></span>

## <span data-ttu-id="32873-170">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32873-170">RELATED LINKS</span></span>
