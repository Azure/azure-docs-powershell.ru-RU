---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A262DFD1-8B90-462C-A4E2-ABA0F51173FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
ms.openlocfilehash: 0cf65c33ca5af99be30f7bfa85ad4ad80ff62735
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566127"
---
# <span data-ttu-id="b1335-101">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b1335-101">Remove-AzureRmResource</span></span>

## <span data-ttu-id="b1335-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b1335-102">SYNOPSIS</span></span>
<span data-ttu-id="b1335-103">Удаляет ресурс.</span><span class="sxs-lookup"><span data-stu-id="b1335-103">Removes a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1335-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b1335-104">SYNTAX</span></span>

### <span data-ttu-id="b1335-105">ByResourceId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b1335-105">ByResourceId (Default)</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1335-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="b1335-106">BySubscriptionLevel</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b1335-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="b1335-107">ByTenantLevel</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1335-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1335-108">DESCRIPTION</span></span>
<span data-ttu-id="b1335-109">Командлет **Remove-AzureRmResource** удаляет ресурс Azure.</span><span class="sxs-lookup"><span data-stu-id="b1335-109">The **Remove-AzureRmResource** cmdlet removes an Azure resource.</span></span>

## <span data-ttu-id="b1335-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b1335-110">EXAMPLES</span></span>

### <span data-ttu-id="b1335-111">Пример 1: Удаление ресурса веб-сайта</span><span class="sxs-lookup"><span data-stu-id="b1335-111">Example 1: Remove a website resource</span></span>
```
PS C:\>Remove-AzureRmResource -ResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/Microsoft.Web/sites/ContosoSite" -Force
```

<span data-ttu-id="b1335-112">Эта команда удаляет ресурс веб-сайта с именем ContosoSite.</span><span class="sxs-lookup"><span data-stu-id="b1335-112">This command removes the website resource named ContosoSite.</span></span>
<span data-ttu-id="b1335-113">В примере используется значение заполнителя для идентификатора подписки.</span><span class="sxs-lookup"><span data-stu-id="b1335-113">The example uses a placeholder value for the subscription ID.</span></span>
<span data-ttu-id="b1335-114">Команда задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="b1335-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="b1335-115">Поэтому он не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="b1335-115">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="b1335-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b1335-116">PARAMETERS</span></span>

### <span data-ttu-id="b1335-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b1335-117">-ApiVersion</span></span>
<span data-ttu-id="b1335-118">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b1335-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="b1335-119">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="b1335-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="b1335-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1335-120">-AsJob</span></span>
<span data-ttu-id="b1335-121">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b1335-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b1335-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1335-122">-DefaultProfile</span></span>
<span data-ttu-id="b1335-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b1335-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b1335-124">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="b1335-124">-ExtensionResourceName</span></span>
<span data-ttu-id="b1335-125">Указывает имя ресурса расширения ресурса, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="b1335-125">Specifies the name of an extension resource of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="b1335-126">Например, чтобы указать базу данных, используйте следующий формат:</span><span class="sxs-lookup"><span data-stu-id="b1335-126">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="b1335-127">имя базы данных сервера доменных имен `/`</span><span class="sxs-lookup"><span data-stu-id="b1335-127">server name`/`database name</span></span>

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

### <span data-ttu-id="b1335-128">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="b1335-128">-ExtensionResourceType</span></span>
<span data-ttu-id="b1335-129">Указывает тип ресурса для расширения ресурса.</span><span class="sxs-lookup"><span data-stu-id="b1335-129">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="b1335-130">Указывает тип ресурса расширения для ресурса.</span><span class="sxs-lookup"><span data-stu-id="b1335-130">Specifies the extension resource type for the resource.</span></span>
<span data-ttu-id="b1335-131">Например:</span><span class="sxs-lookup"><span data-stu-id="b1335-131">For instance:</span></span> 

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

### <span data-ttu-id="b1335-132">-Force</span><span class="sxs-lookup"><span data-stu-id="b1335-132">-Force</span></span>
<span data-ttu-id="b1335-133">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="b1335-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b1335-134">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="b1335-134">-ODataQuery</span></span>
<span data-ttu-id="b1335-135">Задает фильтр стиля Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="b1335-135">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="b1335-136">Этот командлет добавляет это значение в запрос в дополнение к любым другим фильтрам.</span><span class="sxs-lookup"><span data-stu-id="b1335-136">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="b1335-137">-Pre</span><span class="sxs-lookup"><span data-stu-id="b1335-137">-Pre</span></span>
<span data-ttu-id="b1335-138">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="b1335-138">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b1335-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1335-139">-ResourceGroupName</span></span>
<span data-ttu-id="b1335-140">Указывает имя группы ресурсов, из которой этот командлет удаляет ресурс.</span><span class="sxs-lookup"><span data-stu-id="b1335-140">Specifies the name of the resource group from which this cmdlet removes a resource.</span></span>

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

### <span data-ttu-id="b1335-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1335-141">-ResourceId</span></span>
<span data-ttu-id="b1335-142">Указывает полный ИД ресурса, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="b1335-142">Specifies the fully qualified resource ID of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="b1335-143">Идентификатор включает подписку, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="b1335-143">The ID includes the subscription, as in the following example:</span></span> 

<span data-ttu-id="b1335-144">`/subscriptions/`Идентификатор подписки`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="b1335-144">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="b1335-145">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b1335-145">-ResourceName</span></span>
<span data-ttu-id="b1335-146">Указывает имя ресурса, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="b1335-146">Specifies the name of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="b1335-147">Например, чтобы указать базу данных, используйте следующий формат:</span><span class="sxs-lookup"><span data-stu-id="b1335-147">For instance, to specify a database, use the following format:</span></span> 

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

### <span data-ttu-id="b1335-148">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="b1335-148">-ResourceType</span></span>
<span data-ttu-id="b1335-149">Указывает тип ресурса, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="b1335-149">Specifies the type of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="b1335-150">Например, для базы данных тип ресурса выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b1335-150">For instance, for a database, the resource type is as follows:</span></span> 

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

### <span data-ttu-id="b1335-151">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="b1335-151">-TenantLevel</span></span>
<span data-ttu-id="b1335-152">Указывает на то, что этот командлет работает на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="b1335-152">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="b1335-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b1335-153">-Confirm</span></span>
<span data-ttu-id="b1335-154">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b1335-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1335-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1335-155">-WhatIf</span></span>
<span data-ttu-id="b1335-156">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b1335-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1335-157">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b1335-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1335-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1335-158">CommonParameters</span></span>
<span data-ttu-id="b1335-159">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b1335-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1335-160">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1335-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1335-161">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b1335-161">INPUTS</span></span>

### <span data-ttu-id="b1335-162">Ничего</span><span class="sxs-lookup"><span data-stu-id="b1335-162">None</span></span>
<span data-ttu-id="b1335-163">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="b1335-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b1335-164">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1335-164">OUTPUTS</span></span>

### <span data-ttu-id="b1335-165">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b1335-165">System.Boolean</span></span>

## <span data-ttu-id="b1335-166">Пуск</span><span class="sxs-lookup"><span data-stu-id="b1335-166">NOTES</span></span>

## <span data-ttu-id="b1335-167">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b1335-167">RELATED LINKS</span></span>

[<span data-ttu-id="b1335-168">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b1335-168">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="b1335-169">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b1335-169">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="b1335-170">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b1335-170">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="b1335-171">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b1335-171">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="b1335-172">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b1335-172">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


