---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A262DFD1-8B90-462C-A4E2-ABA0F51173FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresource
schema: 2.0.0
ms.openlocfilehash: 29cdde4d48ca782abd680647ed895945062c055d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914998"
---
# <span data-ttu-id="dd037-101">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="dd037-101">Remove-AzureRmResource</span></span>

## <span data-ttu-id="dd037-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dd037-102">SYNOPSIS</span></span>
<span data-ttu-id="dd037-103">Удаляет ресурс.</span><span class="sxs-lookup"><span data-stu-id="dd037-103">Removes a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd037-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dd037-104">SYNTAX</span></span>

### <span data-ttu-id="dd037-105">ByResourceId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dd037-105">ByResourceId (Default)</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd037-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="dd037-106">BySubscriptionLevel</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dd037-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="dd037-107">ByTenantLevel</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd037-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd037-108">DESCRIPTION</span></span>
<span data-ttu-id="dd037-109">Командлет **Remove-AzureRmResource** удаляет ресурс Azure.</span><span class="sxs-lookup"><span data-stu-id="dd037-109">The **Remove-AzureRmResource** cmdlet removes an Azure resource.</span></span>

## <span data-ttu-id="dd037-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dd037-110">EXAMPLES</span></span>

### <span data-ttu-id="dd037-111">Пример 1: Удаление ресурса веб-сайта</span><span class="sxs-lookup"><span data-stu-id="dd037-111">Example 1: Remove a website resource</span></span>
```
PS C:\>Remove-AzureRmResource -ResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/Microsoft.Web/sites/ContosoSite" -Force
```

<span data-ttu-id="dd037-112">Эта команда удаляет ресурс веб-сайта с именем ContosoSite.</span><span class="sxs-lookup"><span data-stu-id="dd037-112">This command removes the website resource named ContosoSite.</span></span>
<span data-ttu-id="dd037-113">В примере используется значение заполнителя для идентификатора подписки.</span><span class="sxs-lookup"><span data-stu-id="dd037-113">The example uses a placeholder value for the subscription ID.</span></span>
<span data-ttu-id="dd037-114">Команда задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="dd037-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="dd037-115">Поэтому он не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="dd037-115">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="dd037-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dd037-116">PARAMETERS</span></span>

### <span data-ttu-id="dd037-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="dd037-117">-ApiVersion</span></span>
<span data-ttu-id="dd037-118">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dd037-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="dd037-119">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="dd037-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="dd037-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd037-120">-AsJob</span></span>
<span data-ttu-id="dd037-121">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="dd037-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dd037-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd037-122">-DefaultProfile</span></span>
<span data-ttu-id="dd037-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="dd037-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dd037-124">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="dd037-124">-ExtensionResourceName</span></span>
<span data-ttu-id="dd037-125">Указывает имя ресурса расширения ресурса, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="dd037-125">Specifies the name of an extension resource of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="dd037-126">Например, чтобы указать базу данных, используйте следующий формат: имя `/` базы данных имени сервера</span><span class="sxs-lookup"><span data-stu-id="dd037-126">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="dd037-127">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="dd037-127">-ExtensionResourceType</span></span>
<span data-ttu-id="dd037-128">Указывает тип ресурса для расширения ресурса.</span><span class="sxs-lookup"><span data-stu-id="dd037-128">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="dd037-129">Указывает тип ресурса расширения для ресурса.</span><span class="sxs-lookup"><span data-stu-id="dd037-129">Specifies the extension resource type for the resource.</span></span>
<span data-ttu-id="dd037-130">Например: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="dd037-130">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="dd037-131">-Force</span><span class="sxs-lookup"><span data-stu-id="dd037-131">-Force</span></span>
<span data-ttu-id="dd037-132">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="dd037-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dd037-133">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="dd037-133">-ODataQuery</span></span>
<span data-ttu-id="dd037-134">Задает фильтр стиля Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="dd037-134">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="dd037-135">Этот командлет добавляет это значение в запрос в дополнение к любым другим фильтрам.</span><span class="sxs-lookup"><span data-stu-id="dd037-135">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="dd037-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="dd037-136">-Pre</span></span>
<span data-ttu-id="dd037-137">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="dd037-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="dd037-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd037-138">-ResourceGroupName</span></span>
<span data-ttu-id="dd037-139">Указывает имя группы ресурсов, из которой этот командлет удаляет ресурс.</span><span class="sxs-lookup"><span data-stu-id="dd037-139">Specifies the name of the resource group from which this cmdlet removes a resource.</span></span>

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

### <span data-ttu-id="dd037-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd037-140">-ResourceId</span></span>
<span data-ttu-id="dd037-141">Указывает полный ИД ресурса, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="dd037-141">Specifies the fully qualified resource ID of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="dd037-142">Идентификатор включает подписку, как показано в следующем примере: `/subscriptions/` ИД подписки`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="dd037-142">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="dd037-143">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="dd037-143">-ResourceName</span></span>
<span data-ttu-id="dd037-144">Указывает имя ресурса, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="dd037-144">Specifies the name of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="dd037-145">Например, чтобы указать базу данных, используйте следующий формат: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="dd037-145">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="dd037-146">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="dd037-146">-ResourceType</span></span>
<span data-ttu-id="dd037-147">Указывает тип ресурса, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="dd037-147">Specifies the type of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="dd037-148">Например, для базы данных тип ресурса выглядит следующим образом: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="dd037-148">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="dd037-149">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="dd037-149">-TenantLevel</span></span>
<span data-ttu-id="dd037-150">Указывает на то, что этот командлет работает на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="dd037-150">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="dd037-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd037-151">-Confirm</span></span>
<span data-ttu-id="dd037-152">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dd037-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd037-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd037-153">-WhatIf</span></span>
<span data-ttu-id="dd037-154">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dd037-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd037-155">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dd037-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd037-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd037-156">CommonParameters</span></span>
<span data-ttu-id="dd037-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dd037-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd037-158">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd037-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd037-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dd037-159">INPUTS</span></span>

### <span data-ttu-id="dd037-160">Ничего</span><span class="sxs-lookup"><span data-stu-id="dd037-160">None</span></span>

## <span data-ttu-id="dd037-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd037-161">OUTPUTS</span></span>

### <span data-ttu-id="dd037-162">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dd037-162">System.Boolean</span></span>

## <span data-ttu-id="dd037-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="dd037-163">NOTES</span></span>

## <span data-ttu-id="dd037-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dd037-164">RELATED LINKS</span></span>



[<span data-ttu-id="dd037-165">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="dd037-165">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="dd037-166">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="dd037-166">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="dd037-167">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="dd037-167">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="dd037-168">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="dd037-168">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


