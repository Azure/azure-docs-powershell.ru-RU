---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/invoke-azurermresourceaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Invoke-AzureRmResourceAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Invoke-AzureRmResourceAction.md
ms.openlocfilehash: 7f2aa8299e3e4dcbdc6d326dfedf76092a65f351
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733233"
---
# <span data-ttu-id="7d6a2-101">Invoke-AzureRmResourceAction</span><span class="sxs-lookup"><span data-stu-id="7d6a2-101">Invoke-AzureRmResourceAction</span></span>

## <span data-ttu-id="7d6a2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7d6a2-102">SYNOPSIS</span></span>
<span data-ttu-id="7d6a2-103">Вызывает действие с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="7d6a2-103">Invokes an action on a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d6a2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7d6a2-104">SYNTAX</span></span>

### <span data-ttu-id="7d6a2-105">ByResourceId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7d6a2-105">ByResourceId (Default)</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String>
 [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7d6a2-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="7d6a2-106">BySubscriptionLevel</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d6a2-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="7d6a2-107">ByTenantLevel</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d6a2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d6a2-108">DESCRIPTION</span></span>
<span data-ttu-id="7d6a2-109">Командлет **Invoke-AzureRmResourceAction** вызывает действие с указанным ресурсом Azure.</span><span class="sxs-lookup"><span data-stu-id="7d6a2-109">The **Invoke-AzureRmResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>

<span data-ttu-id="7d6a2-110">Чтобы получить список поддерживаемых действий, воспользуйтесь средством "Обозреватель ресурсов Azure".</span><span class="sxs-lookup"><span data-stu-id="7d6a2-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="7d6a2-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7d6a2-111">EXAMPLES</span></span>

## <span data-ttu-id="7d6a2-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7d6a2-112">PARAMETERS</span></span>

### <span data-ttu-id="7d6a2-113">-Action (действие)</span><span class="sxs-lookup"><span data-stu-id="7d6a2-113">-Action</span></span>
<span data-ttu-id="7d6a2-114">Указывает имя вызываемого действия.</span><span class="sxs-lookup"><span data-stu-id="7d6a2-114">Specifies the name of the action to invoke.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ActionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6a2-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7d6a2-115">-ApiVersion</span></span>
<span data-ttu-id="7d6a2-116">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7d6a2-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="7d6a2-117">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="7d6a2-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6a2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d6a2-118">-DefaultProfile</span></span>
<span data-ttu-id="7d6a2-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7d6a2-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6a2-120">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="7d6a2-120">-ExtensionResourceName</span></span>
<span data-ttu-id="7d6a2-121">Указывает имя ресурса расширения для ресурса, в котором этот командлет вызывает действие.</span><span class="sxs-lookup"><span data-stu-id="7d6a2-121">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="7d6a2-122">Например, чтобы указать базу данных, используйте следующий формат:</span><span class="sxs-lookup"><span data-stu-id="7d6a2-122">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="7d6a2-123">имя базы данных сервера доменных имен `/`</span><span class="sxs-lookup"><span data-stu-id="7d6a2-123">server name`/`database name</span></span>

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d6a2-124">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="7d6a2-124">-ExtensionResourceType</span></span>
<span data-ttu-id="7d6a2-125">Указывает тип ресурса расширения.</span><span class="sxs-lookup"><span data-stu-id="7d6a2-125">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="7d6a2-126">Например:</span><span class="sxs-lookup"><span data-stu-id="7d6a2-126">For instance:</span></span> 

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d6a2-127">-Force</span><span class="sxs-lookup"><span data-stu-id="7d6a2-127">-Force</span></span>
<span data-ttu-id="7d6a2-128">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="7d6a2-128">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6a2-129">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="7d6a2-129">-InformationAction</span></span>
<span data-ttu-id="7d6a2-130">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="7d6a2-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7d6a2-131">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="7d6a2-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7d6a2-132">Продолжал</span><span class="sxs-lookup"><span data-stu-id="7d6a2-132">Continue</span></span>
- <span data-ttu-id="7d6a2-133">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="7d6a2-133">Ignore</span></span>
- <span data-ttu-id="7d6a2-134">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="7d6a2-134">Inquire</span></span>
- <span data-ttu-id="7d6a2-135">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7d6a2-135">SilentlyContinue</span></span>
- <span data-ttu-id="7d6a2-136">Остановить</span><span class="sxs-lookup"><span data-stu-id="7d6a2-136">Stop</span></span>
- <span data-ttu-id="7d6a2-137">Рвать</span><span class="sxs-lookup"><span data-stu-id="7d6a2-137">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6a2-138">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7d6a2-138">-InformationVariable</span></span>
<span data-ttu-id="7d6a2-139">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="7d6a2-139">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6a2-140">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="7d6a2-140">-ODataQuery</span></span>
<span data-ttu-id="7d6a2-141">Задает фильтр стиля Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="7d6a2-141">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="7d6a2-142">Этот командлет добавляет это значение в запрос в дополнение к любым другим фильтрам.</span><span class="sxs-lookup"><span data-stu-id="7d6a2-142">This cmdlet appends this value to the request in addition to any other filters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6a2-143">-Parameters</span><span class="sxs-lookup"><span data-stu-id="7d6a2-143">-Parameters</span></span>
<span data-ttu-id="7d6a2-144">Задает параметры, которые являются хэш-таблицами для действия, вызванного этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="7d6a2-144">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Object

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6a2-145">-Pre</span><span class="sxs-lookup"><span data-stu-id="7d6a2-145">-Pre</span></span>
<span data-ttu-id="7d6a2-146">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="7d6a2-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6a2-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d6a2-147">-ResourceGroupName</span></span>
<span data-ttu-id="7d6a2-148">Указывает имя группы ресурсов, в которой этот командлет вызывает действие.</span><span class="sxs-lookup"><span data-stu-id="7d6a2-148">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

```yaml
Type: String
Parameter Sets: BySubscriptionLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d6a2-149">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d6a2-149">-ResourceId</span></span>
<span data-ttu-id="7d6a2-150">Указывает полный ИД ресурса ресурса, в котором этот командлет вызывает действие.</span><span class="sxs-lookup"><span data-stu-id="7d6a2-150">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="7d6a2-151">Идентификатор включает подписку, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="7d6a2-151">The ID includes the subscription, as in the following example:</span></span> 

<span data-ttu-id="7d6a2-152">`/subscriptions/`Идентификатор подписки`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="7d6a2-152">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d6a2-153">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="7d6a2-153">-ResourceName</span></span>
<span data-ttu-id="7d6a2-154">Указывает имя ресурса ресурса, который этот командлет вызывает действие.</span><span class="sxs-lookup"><span data-stu-id="7d6a2-154">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="7d6a2-155">Например, чтобы указать базу данных, используйте следующий формат:</span><span class="sxs-lookup"><span data-stu-id="7d6a2-155">For instance, to specify a database, use the following format:</span></span> 

`ContosoServer/ContosoDatabase`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d6a2-156">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="7d6a2-156">-ResourceType</span></span>
<span data-ttu-id="7d6a2-157">Указывает тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="7d6a2-157">Specifies the type of the resource.</span></span>
<span data-ttu-id="7d6a2-158">Например, для базы данных тип ресурса выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="7d6a2-158">For instance, for a database, the resource type is as follows:</span></span> 

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d6a2-159">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="7d6a2-159">-TenantLevel</span></span>
<span data-ttu-id="7d6a2-160">Указывает на то, что этот командлет работает на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="7d6a2-160">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6a2-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7d6a2-161">-Confirm</span></span>
<span data-ttu-id="7d6a2-162">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7d6a2-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6a2-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d6a2-163">-WhatIf</span></span>
<span data-ttu-id="7d6a2-164">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7d6a2-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d6a2-165">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7d6a2-165">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6a2-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d6a2-166">CommonParameters</span></span>
<span data-ttu-id="7d6a2-167">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7d6a2-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d6a2-168">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d6a2-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d6a2-169">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7d6a2-169">INPUTS</span></span>

### <span data-ttu-id="7d6a2-170">Ничего</span><span class="sxs-lookup"><span data-stu-id="7d6a2-170">None</span></span>
<span data-ttu-id="7d6a2-171">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="7d6a2-171">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7d6a2-172">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d6a2-172">OUTPUTS</span></span>

### <span data-ttu-id="7d6a2-173">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="7d6a2-173">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="7d6a2-174">Пуск</span><span class="sxs-lookup"><span data-stu-id="7d6a2-174">NOTES</span></span>

## <span data-ttu-id="7d6a2-175">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7d6a2-175">RELATED LINKS</span></span>
