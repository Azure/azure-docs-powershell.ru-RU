---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A262DFD1-8B90-462C-A4E2-ABA0F51173FA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
ms.openlocfilehash: 92d6fc81536568b2654fb72a1d6462830c05923e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567062"
---
# <span data-ttu-id="6cc8b-101">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="6cc8b-101">Remove-AzureRmResource</span></span>

## <span data-ttu-id="6cc8b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6cc8b-102">SYNOPSIS</span></span>
<span data-ttu-id="6cc8b-103">Удаляет ресурс.</span><span class="sxs-lookup"><span data-stu-id="6cc8b-103">Removes a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6cc8b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6cc8b-104">SYNTAX</span></span>

### <span data-ttu-id="6cc8b-105">Идентификатор ресурса (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="6cc8b-105">The resource Id. (Default)</span></span>
```
Remove-AzureRmResource -ResourceId <String> [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cc8b-106">Ресурс, находящийся на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="6cc8b-106">Resource that resides at the subscription level.</span></span>
```
Remove-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6cc8b-107">Ресурс, находящийся на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="6cc8b-107">Resource that resides at the tenant level.</span></span>
```
Remove-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cc8b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6cc8b-108">DESCRIPTION</span></span>
<span data-ttu-id="6cc8b-109">Командлет **Remove-AzureRmResource** удаляет ресурс Azure.</span><span class="sxs-lookup"><span data-stu-id="6cc8b-109">The **Remove-AzureRmResource** cmdlet removes an Azure resource.</span></span>

## <span data-ttu-id="6cc8b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6cc8b-110">EXAMPLES</span></span>

### <span data-ttu-id="6cc8b-111">Пример 1: Удаление ресурса веб-сайта</span><span class="sxs-lookup"><span data-stu-id="6cc8b-111">Example 1: Remove a website resource</span></span>
```
PS C:\>Remove-AzureRmResource -ResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/Microsoft.Web/sites/ContosoSite" -Force
```

<span data-ttu-id="6cc8b-112">Эта команда удаляет ресурс веб-сайта с именем ContosoSite.</span><span class="sxs-lookup"><span data-stu-id="6cc8b-112">This command removes the website resource named ContosoSite.</span></span>
<span data-ttu-id="6cc8b-113">В примере используется значение заполнителя для идентификатора подписки.</span><span class="sxs-lookup"><span data-stu-id="6cc8b-113">The example uses a placeholder value for the subscription ID.</span></span>
<span data-ttu-id="6cc8b-114">Команда задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="6cc8b-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="6cc8b-115">Поэтому он не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="6cc8b-115">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="6cc8b-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6cc8b-116">PARAMETERS</span></span>

### <span data-ttu-id="6cc8b-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6cc8b-117">-ApiVersion</span></span>
<span data-ttu-id="6cc8b-118">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6cc8b-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="6cc8b-119">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="6cc8b-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="6cc8b-120">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="6cc8b-120">-ExtensionResourceName</span></span>
<span data-ttu-id="6cc8b-121">Указывает имя ресурса расширения ресурса, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="6cc8b-121">Specifies the name of an extension resource of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="6cc8b-122">Например, чтобы указать базу данных, используйте следующий формат:</span><span class="sxs-lookup"><span data-stu-id="6cc8b-122">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="6cc8b-123">имя базы данных сервера доменных имен `/`</span><span class="sxs-lookup"><span data-stu-id="6cc8b-123">server name`/`database name</span></span>

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc8b-124">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="6cc8b-124">-ExtensionResourceType</span></span>
<span data-ttu-id="6cc8b-125">Указывает тип ресурса для расширения ресурса.</span><span class="sxs-lookup"><span data-stu-id="6cc8b-125">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="6cc8b-126">Указывает тип ресурса расширения для ресурса.</span><span class="sxs-lookup"><span data-stu-id="6cc8b-126">Specifies the extension resource type for the resource.</span></span>
<span data-ttu-id="6cc8b-127">Например:</span><span class="sxs-lookup"><span data-stu-id="6cc8b-127">For instance:</span></span> 

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc8b-128">-Force</span><span class="sxs-lookup"><span data-stu-id="6cc8b-128">-Force</span></span>
<span data-ttu-id="6cc8b-129">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="6cc8b-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6cc8b-130">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="6cc8b-130">-ODataQuery</span></span>
<span data-ttu-id="6cc8b-131">Задает фильтр стиля Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="6cc8b-131">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="6cc8b-132">Этот командлет добавляет это значение в запрос в дополнение к любым другим фильтрам.</span><span class="sxs-lookup"><span data-stu-id="6cc8b-132">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="6cc8b-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="6cc8b-133">-Pre</span></span>
<span data-ttu-id="6cc8b-134">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="6cc8b-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6cc8b-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cc8b-135">-ResourceGroupName</span></span>
<span data-ttu-id="6cc8b-136">Указывает имя группы ресурсов, из которой этот командлет удаляет ресурс.</span><span class="sxs-lookup"><span data-stu-id="6cc8b-136">Specifies the name of the resource group from which this cmdlet removes a resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc8b-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6cc8b-137">-ResourceId</span></span>
<span data-ttu-id="6cc8b-138">Указывает полный ИД ресурса, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="6cc8b-138">Specifies the fully qualified resource ID of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="6cc8b-139">Идентификатор включает подписку, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="6cc8b-139">The ID includes the subscription, as in the following example:</span></span> 

<span data-ttu-id="6cc8b-140">`/subscriptions/`Идентификатор подписки`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="6cc8b-140">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: The resource Id.
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc8b-141">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="6cc8b-141">-ResourceName</span></span>
<span data-ttu-id="6cc8b-142">Указывает имя ресурса, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="6cc8b-142">Specifies the name of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="6cc8b-143">Например, чтобы указать базу данных, используйте следующий формат:</span><span class="sxs-lookup"><span data-stu-id="6cc8b-143">For instance, to specify a database, use the following format:</span></span> 

`ContosoServer/ContosoDatabase`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc8b-144">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="6cc8b-144">-ResourceType</span></span>
<span data-ttu-id="6cc8b-145">Указывает тип ресурса, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="6cc8b-145">Specifies the type of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="6cc8b-146">Например, для базы данных тип ресурса выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="6cc8b-146">For instance, for a database, the resource type is as follows:</span></span> 

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc8b-147">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="6cc8b-147">-TenantLevel</span></span>
<span data-ttu-id="6cc8b-148">Указывает на то, что этот командлет работает на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="6cc8b-148">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Resource that resides at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cc8b-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6cc8b-149">-Confirm</span></span>
<span data-ttu-id="6cc8b-150">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6cc8b-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cc8b-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cc8b-151">-WhatIf</span></span>
<span data-ttu-id="6cc8b-152">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6cc8b-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cc8b-153">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6cc8b-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cc8b-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cc8b-154">-DefaultProfile</span></span>
<span data-ttu-id="6cc8b-155">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6cc8b-155">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cc8b-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cc8b-156">CommonParameters</span></span>
<span data-ttu-id="6cc8b-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6cc8b-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cc8b-158">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cc8b-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cc8b-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6cc8b-159">INPUTS</span></span>

## <span data-ttu-id="6cc8b-160">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6cc8b-160">OUTPUTS</span></span>

### <span data-ttu-id="6cc8b-161">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6cc8b-161">System.Boolean</span></span>

## <span data-ttu-id="6cc8b-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="6cc8b-162">NOTES</span></span>

## <span data-ttu-id="6cc8b-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6cc8b-163">RELATED LINKS</span></span>

[<span data-ttu-id="6cc8b-164">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="6cc8b-164">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="6cc8b-165">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="6cc8b-165">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="6cc8b-166">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="6cc8b-166">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="6cc8b-167">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="6cc8b-167">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="6cc8b-168">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="6cc8b-168">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


