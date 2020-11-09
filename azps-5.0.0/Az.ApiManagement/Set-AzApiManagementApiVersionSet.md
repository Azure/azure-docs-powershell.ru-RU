---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
ms.openlocfilehash: d85d480adc5d6c588c7da2f03c514258dc96a9e8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316778"
---
# <span data-ttu-id="36d39-101">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="36d39-101">Set-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="36d39-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="36d39-102">SYNOPSIS</span></span>
<span data-ttu-id="36d39-103">Обновляет наборы API в контексте управления API.</span><span class="sxs-lookup"><span data-stu-id="36d39-103">Updates an API Version Set in the API Management Context.</span></span>

## <span data-ttu-id="36d39-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="36d39-104">SYNTAX</span></span>

### <span data-ttu-id="36d39-105">ExpandedParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="36d39-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="36d39-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="36d39-106">ByInputObject</span></span>
```
Set-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="36d39-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="36d39-107">DESCRIPTION</span></span>

<span data-ttu-id="36d39-108">Командлет **Set-AzApiManagementApiVersionSet** изменяет версию API Azure API Management Set.</span><span class="sxs-lookup"><span data-stu-id="36d39-108">The **Set-AzApiManagementApiVersionSet** cmdlet modifies an Azure API Management API Version Set.</span></span>

## <span data-ttu-id="36d39-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="36d39-109">EXAMPLES</span></span>

### <span data-ttu-id="36d39-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="36d39-110">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId "query-verion-set" -Scheme Header -HeaderName "api-version" -Description "Azure version header string"
```

<span data-ttu-id="36d39-111">Эта команда обновляет существующий комплект API, установленный в схеме управления версиями `Header` и параметром заголовков `api-version` .</span><span class="sxs-lookup"><span data-stu-id="36d39-111">This command updates an existing API Version Set with versioning scheme `Header` and Header parameter `api-version`.</span></span>

## <span data-ttu-id="36d39-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="36d39-112">PARAMETERS</span></span>

### <span data-ttu-id="36d39-113">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="36d39-113">-ApiVersionSetId</span></span>
<span data-ttu-id="36d39-114">Идентификатор для нового множества версий API.</span><span class="sxs-lookup"><span data-stu-id="36d39-114">Identifier for new API Version Set.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36d39-115">-Context</span><span class="sxs-lookup"><span data-stu-id="36d39-115">-Context</span></span>
<span data-ttu-id="36d39-116">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="36d39-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="36d39-117">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="36d39-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36d39-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36d39-118">-DefaultProfile</span></span>
<span data-ttu-id="36d39-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="36d39-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36d39-120">-Описание</span><span class="sxs-lookup"><span data-stu-id="36d39-120">-Description</span></span>
<span data-ttu-id="36d39-121">Описание набора версий API.</span><span class="sxs-lookup"><span data-stu-id="36d39-121">Description of the Api Version set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36d39-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="36d39-122">-HeaderName</span></span>
<span data-ttu-id="36d39-123">Значение заголовка, которое будет содержать сведения о версии.</span><span class="sxs-lookup"><span data-stu-id="36d39-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="36d39-124">Если выбран заголовок схема управления версиями, необходимо указать это значение.</span><span class="sxs-lookup"><span data-stu-id="36d39-124">If versioning Scheme HEADER is chosen, then this value must be specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36d39-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36d39-125">-InputObject</span></span>
<span data-ttu-id="36d39-126">Экземпляр PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="36d39-126">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="36d39-127">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="36d39-127">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36d39-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="36d39-128">-Name</span></span>
<span data-ttu-id="36d39-129">Имя набора ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="36d39-129">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="36d39-130">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="36d39-130">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36d39-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36d39-131">-PassThru</span></span>
<span data-ttu-id="36d39-132">Если указан, то экземпляр типа Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiVersionSet, который представляет измененный apiVersionSet, будет записываться в Output.</span><span class="sxs-lookup"><span data-stu-id="36d39-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet type  representing the modified apiVersionSet will be written to output.</span></span>

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

### <span data-ttu-id="36d39-133">-QueryName</span><span class="sxs-lookup"><span data-stu-id="36d39-133">-QueryName</span></span>
<span data-ttu-id="36d39-134">Значение запроса, в котором будут содержаться сведения о версиях.</span><span class="sxs-lookup"><span data-stu-id="36d39-134">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="36d39-135">Если выбран запрос на схему управления версиями, необходимо указать это значение.</span><span class="sxs-lookup"><span data-stu-id="36d39-135">If versioning Scheme Query is chosen, then this value must be specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36d39-136">-Схема</span><span class="sxs-lookup"><span data-stu-id="36d39-136">-Scheme</span></span>
<span data-ttu-id="36d39-137">Схема управления версиями, которую нужно выбрать для наборов версий API.</span><span class="sxs-lookup"><span data-stu-id="36d39-137">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="36d39-138">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="36d39-138">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme
Parameter Sets: (All)
Aliases:
Accepted values: Segment, Query, Header

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36d39-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36d39-139">-Confirm</span></span>
<span data-ttu-id="36d39-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="36d39-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36d39-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36d39-141">-WhatIf</span></span>
<span data-ttu-id="36d39-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="36d39-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36d39-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="36d39-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36d39-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36d39-144">CommonParameters</span></span>
<span data-ttu-id="36d39-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="36d39-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36d39-146">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36d39-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36d39-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="36d39-147">INPUTS</span></span>

### <span data-ttu-id="36d39-148">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="36d39-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="36d39-149">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="36d39-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="36d39-150">System. String</span><span class="sxs-lookup"><span data-stu-id="36d39-150">System.String</span></span>

### <span data-ttu-id="36d39-151">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="36d39-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="36d39-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="36d39-152">OUTPUTS</span></span>

### <span data-ttu-id="36d39-153">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="36d39-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="36d39-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="36d39-154">NOTES</span></span>

## <span data-ttu-id="36d39-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="36d39-155">RELATED LINKS</span></span>

[<span data-ttu-id="36d39-156">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="36d39-156">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="36d39-157">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="36d39-157">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="36d39-158">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="36d39-158">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)
