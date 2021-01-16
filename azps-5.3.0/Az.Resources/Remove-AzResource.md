---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: A262DFD1-8B90-462C-A4E2-ABA0F51173FA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResource.md
ms.openlocfilehash: 31039d71f0c26b6fea3e19220b3932d2abd02073
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506705"
---
# <span data-ttu-id="43bb4-101">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="43bb4-101">Remove-AzResource</span></span>

## <span data-ttu-id="43bb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43bb4-102">SYNOPSIS</span></span>
<span data-ttu-id="43bb4-103">Удаляет ресурс.</span><span class="sxs-lookup"><span data-stu-id="43bb4-103">Removes a resource.</span></span>

## <span data-ttu-id="43bb4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="43bb4-104">SYNTAX</span></span>

### <span data-ttu-id="43bb4-105">ByResourceId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="43bb4-105">ByResourceId (Default)</span></span>
```
Remove-AzResource [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43bb4-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="43bb4-106">BySubscriptionLevel</span></span>
```
Remove-AzResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="43bb4-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="43bb4-107">ByTenantLevel</span></span>
```
Remove-AzResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43bb4-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="43bb4-108">DESCRIPTION</span></span>
<span data-ttu-id="43bb4-109">С **его использованием** удаляется ресурс Azure.</span><span class="sxs-lookup"><span data-stu-id="43bb4-109">The **Remove-AzResource** cmdlet removes an Azure resource.</span></span>

## <span data-ttu-id="43bb4-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="43bb4-110">EXAMPLES</span></span>

### <span data-ttu-id="43bb4-111">Пример 1. Удаление ресурса веб-сайта</span><span class="sxs-lookup"><span data-stu-id="43bb4-111">Example 1: Remove a website resource</span></span>
```
PS C:\>Remove-AzResource -ResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/Microsoft.Web/sites/ContosoSite" -Force
```

<span data-ttu-id="43bb4-112">Эта команда удаляет ресурс веб-сайта ContosoSite.</span><span class="sxs-lookup"><span data-stu-id="43bb4-112">This command removes the website resource named ContosoSite.</span></span>
<span data-ttu-id="43bb4-113">В примере используется заме желтая стоимость для ИД подписки.</span><span class="sxs-lookup"><span data-stu-id="43bb4-113">The example uses a placeholder value for the subscription ID.</span></span>
<span data-ttu-id="43bb4-114">Команда определяет параметр *Force.*</span><span class="sxs-lookup"><span data-stu-id="43bb4-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="43bb4-115">Поэтому запрос на подтверждение не будет.</span><span class="sxs-lookup"><span data-stu-id="43bb4-115">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="43bb4-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43bb4-116">PARAMETERS</span></span>

### <span data-ttu-id="43bb4-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="43bb4-117">-ApiVersion</span></span>
<span data-ttu-id="43bb4-118">Определяет версию API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="43bb4-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="43bb4-119">Если не указать версию, этот cmdlet использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="43bb4-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="43bb4-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43bb4-120">-AsJob</span></span>
<span data-ttu-id="43bb4-121">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="43bb4-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="43bb4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43bb4-122">-DefaultProfile</span></span>
<span data-ttu-id="43bb4-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="43bb4-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43bb4-124">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="43bb4-124">-ExtensionResourceName</span></span>
<span data-ttu-id="43bb4-125">Указывает имя ресурса расширения для ресурса, который удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43bb4-125">Specifies the name of an extension resource of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="43bb4-126">Например, чтобы указать базу данных, используйте следующий формат: имя `/` базы данных "Имя сервера".</span><span class="sxs-lookup"><span data-stu-id="43bb4-126">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="43bb4-127">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="43bb4-127">-ExtensionResourceType</span></span>
<span data-ttu-id="43bb4-128">Тип ресурса для ресурса расширения.</span><span class="sxs-lookup"><span data-stu-id="43bb4-128">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="43bb4-129">Тип ресурса расширения.</span><span class="sxs-lookup"><span data-stu-id="43bb4-129">Specifies the extension resource type for the resource.</span></span>
<span data-ttu-id="43bb4-130">Например: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="43bb4-130">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="43bb4-131">-Force</span><span class="sxs-lookup"><span data-stu-id="43bb4-131">-Force</span></span>
<span data-ttu-id="43bb4-132">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="43bb4-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="43bb4-133">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="43bb4-133">-ODataQuery</span></span>
<span data-ttu-id="43bb4-134">Указывает фильтр стилей Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="43bb4-134">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="43bb4-135">Этот cmdlet добавит это значение к запросу в дополнение к любым другим фильтрам.</span><span class="sxs-lookup"><span data-stu-id="43bb4-135">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="43bb4-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="43bb4-136">-Pre</span></span>
<span data-ttu-id="43bb4-137">Указывает на то, что этот cmdlet рассматривает предварительные версии API при автоматическом определении используемой версии.</span><span class="sxs-lookup"><span data-stu-id="43bb4-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="43bb4-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43bb4-138">-ResourceGroupName</span></span>
<span data-ttu-id="43bb4-139">Имя группы ресурсов, из которой этот cmdlet удаляет ресурс.</span><span class="sxs-lookup"><span data-stu-id="43bb4-139">Specifies the name of the resource group from which this cmdlet removes a resource.</span></span>

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

### <span data-ttu-id="43bb4-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43bb4-140">-ResourceId</span></span>
<span data-ttu-id="43bb4-141">Определяет полное ид ресурса, который удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43bb4-141">Specifies the fully qualified resource ID of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="43bb4-142">ИД включает подписку, как в следующем примере: `/subscriptions/` ИД подписки`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="43bb4-142">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="43bb4-143">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="43bb4-143">-ResourceName</span></span>
<span data-ttu-id="43bb4-144">Указывает имя ресурса, который удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43bb4-144">Specifies the name of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="43bb4-145">Например, чтобы указать базу данных, используйте следующий формат: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="43bb4-145">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="43bb4-146">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="43bb4-146">-ResourceType</span></span>
<span data-ttu-id="43bb4-147">Определяет тип ресурса, который удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43bb4-147">Specifies the type of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="43bb4-148">Например, для базы данных тип ресурса: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="43bb4-148">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="43bb4-149">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="43bb4-149">-TenantLevel</span></span>
<span data-ttu-id="43bb4-150">Указывает на то, что этот cmdlet выполняется на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="43bb4-150">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="43bb4-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43bb4-151">-Confirm</span></span>
<span data-ttu-id="43bb4-152">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="43bb4-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43bb4-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43bb4-153">-WhatIf</span></span>
<span data-ttu-id="43bb4-154">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43bb4-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43bb4-155">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="43bb4-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43bb4-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43bb4-156">CommonParameters</span></span>
<span data-ttu-id="43bb4-157">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43bb4-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43bb4-158">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="43bb4-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43bb4-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="43bb4-159">INPUTS</span></span>

### <span data-ttu-id="43bb4-160">System.String</span><span class="sxs-lookup"><span data-stu-id="43bb4-160">System.String</span></span>

## <span data-ttu-id="43bb4-161">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="43bb4-161">OUTPUTS</span></span>

### <span data-ttu-id="43bb4-162">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="43bb4-162">System.Boolean</span></span>

## <span data-ttu-id="43bb4-163">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="43bb4-163">NOTES</span></span>

## <span data-ttu-id="43bb4-164">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="43bb4-164">RELATED LINKS</span></span>

[<span data-ttu-id="43bb4-165">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="43bb4-165">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="43bb4-166">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="43bb4-166">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="43bb4-167">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="43bb4-167">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="43bb4-168">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="43bb4-168">Set-AzResource</span></span>](./Set-AzResource.md)


