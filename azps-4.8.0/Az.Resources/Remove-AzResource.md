---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: A262DFD1-8B90-462C-A4E2-ABA0F51173FA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResource.md
ms.openlocfilehash: ecd70916f1ddb6e365fb9f880db9974f6c9ae771
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235416"
---
# <span data-ttu-id="fe08d-101">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="fe08d-101">Remove-AzResource</span></span>

## <span data-ttu-id="fe08d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fe08d-102">SYNOPSIS</span></span>
<span data-ttu-id="fe08d-103">Удаляет ресурс.</span><span class="sxs-lookup"><span data-stu-id="fe08d-103">Removes a resource.</span></span>

## <span data-ttu-id="fe08d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fe08d-104">SYNTAX</span></span>

### <span data-ttu-id="fe08d-105">ByResourceId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fe08d-105">ByResourceId (Default)</span></span>
```
Remove-AzResource [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe08d-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="fe08d-106">BySubscriptionLevel</span></span>
```
Remove-AzResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fe08d-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="fe08d-107">ByTenantLevel</span></span>
```
Remove-AzResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe08d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe08d-108">DESCRIPTION</span></span>
<span data-ttu-id="fe08d-109">Командлет **Remove-AzResource** удаляет ресурс Azure.</span><span class="sxs-lookup"><span data-stu-id="fe08d-109">The **Remove-AzResource** cmdlet removes an Azure resource.</span></span>

## <span data-ttu-id="fe08d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fe08d-110">EXAMPLES</span></span>

### <span data-ttu-id="fe08d-111">Пример 1: Удаление ресурса веб-сайта</span><span class="sxs-lookup"><span data-stu-id="fe08d-111">Example 1: Remove a website resource</span></span>
```
PS C:\>Remove-AzResource -ResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/Microsoft.Web/sites/ContosoSite" -Force
```

<span data-ttu-id="fe08d-112">Эта команда удаляет ресурс веб-сайта с именем ContosoSite.</span><span class="sxs-lookup"><span data-stu-id="fe08d-112">This command removes the website resource named ContosoSite.</span></span>
<span data-ttu-id="fe08d-113">В примере используется значение заполнителя для идентификатора подписки.</span><span class="sxs-lookup"><span data-stu-id="fe08d-113">The example uses a placeholder value for the subscription ID.</span></span>
<span data-ttu-id="fe08d-114">Команда задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="fe08d-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="fe08d-115">Поэтому он не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="fe08d-115">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="fe08d-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fe08d-116">PARAMETERS</span></span>

### <span data-ttu-id="fe08d-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="fe08d-117">-ApiVersion</span></span>
<span data-ttu-id="fe08d-118">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fe08d-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="fe08d-119">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="fe08d-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="fe08d-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe08d-120">-AsJob</span></span>
<span data-ttu-id="fe08d-121">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="fe08d-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fe08d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe08d-122">-DefaultProfile</span></span>
<span data-ttu-id="fe08d-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="fe08d-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe08d-124">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="fe08d-124">-ExtensionResourceName</span></span>
<span data-ttu-id="fe08d-125">Указывает имя ресурса расширения ресурса, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="fe08d-125">Specifies the name of an extension resource of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="fe08d-126">Например, чтобы указать базу данных, используйте следующий формат: имя `/` базы данных имени сервера</span><span class="sxs-lookup"><span data-stu-id="fe08d-126">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="fe08d-127">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="fe08d-127">-ExtensionResourceType</span></span>
<span data-ttu-id="fe08d-128">Указывает тип ресурса для расширения ресурса.</span><span class="sxs-lookup"><span data-stu-id="fe08d-128">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="fe08d-129">Указывает тип ресурса расширения для ресурса.</span><span class="sxs-lookup"><span data-stu-id="fe08d-129">Specifies the extension resource type for the resource.</span></span>
<span data-ttu-id="fe08d-130">Например: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="fe08d-130">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="fe08d-131">-Force</span><span class="sxs-lookup"><span data-stu-id="fe08d-131">-Force</span></span>
<span data-ttu-id="fe08d-132">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="fe08d-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fe08d-133">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="fe08d-133">-ODataQuery</span></span>
<span data-ttu-id="fe08d-134">Задает фильтр стиля Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="fe08d-134">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="fe08d-135">Этот командлет добавляет это значение в запрос в дополнение к любым другим фильтрам.</span><span class="sxs-lookup"><span data-stu-id="fe08d-135">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="fe08d-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="fe08d-136">-Pre</span></span>
<span data-ttu-id="fe08d-137">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="fe08d-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="fe08d-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe08d-138">-ResourceGroupName</span></span>
<span data-ttu-id="fe08d-139">Указывает имя группы ресурсов, из которой этот командлет удаляет ресурс.</span><span class="sxs-lookup"><span data-stu-id="fe08d-139">Specifies the name of the resource group from which this cmdlet removes a resource.</span></span>

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

### <span data-ttu-id="fe08d-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe08d-140">-ResourceId</span></span>
<span data-ttu-id="fe08d-141">Указывает полный ИД ресурса, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="fe08d-141">Specifies the fully qualified resource ID of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="fe08d-142">Идентификатор включает подписку, как показано в следующем примере: `/subscriptions/` ИД подписки`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="fe08d-142">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="fe08d-143">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="fe08d-143">-ResourceName</span></span>
<span data-ttu-id="fe08d-144">Указывает имя ресурса, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="fe08d-144">Specifies the name of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="fe08d-145">Например, чтобы указать базу данных, используйте следующий формат: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="fe08d-145">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="fe08d-146">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="fe08d-146">-ResourceType</span></span>
<span data-ttu-id="fe08d-147">Указывает тип ресурса, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="fe08d-147">Specifies the type of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="fe08d-148">Например, для базы данных тип ресурса выглядит следующим образом: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="fe08d-148">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="fe08d-149">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="fe08d-149">-TenantLevel</span></span>
<span data-ttu-id="fe08d-150">Указывает на то, что этот командлет работает на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="fe08d-150">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="fe08d-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe08d-151">-Confirm</span></span>
<span data-ttu-id="fe08d-152">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fe08d-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe08d-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe08d-153">-WhatIf</span></span>
<span data-ttu-id="fe08d-154">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fe08d-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe08d-155">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fe08d-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe08d-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe08d-156">CommonParameters</span></span>
<span data-ttu-id="fe08d-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fe08d-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe08d-158">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe08d-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe08d-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fe08d-159">INPUTS</span></span>

### <span data-ttu-id="fe08d-160">System. String</span><span class="sxs-lookup"><span data-stu-id="fe08d-160">System.String</span></span>

## <span data-ttu-id="fe08d-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe08d-161">OUTPUTS</span></span>

### <span data-ttu-id="fe08d-162">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fe08d-162">System.Boolean</span></span>

## <span data-ttu-id="fe08d-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="fe08d-163">NOTES</span></span>

## <span data-ttu-id="fe08d-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fe08d-164">RELATED LINKS</span></span>

[<span data-ttu-id="fe08d-165">Find-AzResource</span><span class="sxs-lookup"><span data-stu-id="fe08d-165">Find-AzResource</span></span>](./Find-AzResource.md)

[<span data-ttu-id="fe08d-166">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="fe08d-166">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="fe08d-167">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="fe08d-167">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="fe08d-168">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="fe08d-168">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="fe08d-169">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="fe08d-169">Set-AzResource</span></span>](./Set-AzResource.md)


