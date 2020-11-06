---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApiVersionSet.md
ms.openlocfilehash: 5d9bc89eb2d4188b7b2903bee7a8b0a44bec1216
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565963"
---
# <span data-ttu-id="dde0a-101">Set-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="dde0a-101">Set-AzureRmApiManagementApiVersionSet</span></span>

## <span data-ttu-id="dde0a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dde0a-102">SYNOPSIS</span></span>
<span data-ttu-id="dde0a-103">Обновляет наборы API в контексте управления API.</span><span class="sxs-lookup"><span data-stu-id="dde0a-103">Updates an API Version Set in the API Management Context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dde0a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dde0a-104">SYNTAX</span></span>

### <span data-ttu-id="dde0a-105">ExpandedParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dde0a-105">ExpandedParameter (Default)</span></span>
```
Set-AzureRmApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String>
 [-Name <String>] [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dde0a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="dde0a-106">ByInputObject</span></span>
```
Set-AzureRmApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dde0a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dde0a-107">DESCRIPTION</span></span>

<span data-ttu-id="dde0a-108">Командлет **Set-AzureRmApiManagementApiVersionSet** изменяет версию API Azure API Management Set.</span><span class="sxs-lookup"><span data-stu-id="dde0a-108">The **Set-AzureRmApiManagementApiVersionSet** cmdlet modifies an Azure API Management API Version Set.</span></span>

## <span data-ttu-id="dde0a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dde0a-109">EXAMPLES</span></span>

### <span data-ttu-id="dde0a-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dde0a-110">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId "query-verion-set" -Scheme Header -HeaderName "api-version" -Description "Azure version header string"
```

<span data-ttu-id="dde0a-111">Эта команда обновляет существующий комплект API, установленный в схеме управления версиями `Header` и параметром заголовков `api-version` .</span><span class="sxs-lookup"><span data-stu-id="dde0a-111">This command updates an existing API Version Set with versioning scheme `Header` and Header parameter `api-version`.</span></span>

## <span data-ttu-id="dde0a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dde0a-112">PARAMETERS</span></span>

### <span data-ttu-id="dde0a-113">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="dde0a-113">-ApiVersionSetId</span></span>
<span data-ttu-id="dde0a-114">Идентификатор для нового множества версий API.</span><span class="sxs-lookup"><span data-stu-id="dde0a-114">Identifier for new API Version Set.</span></span>

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

### <span data-ttu-id="dde0a-115">-Context</span><span class="sxs-lookup"><span data-stu-id="dde0a-115">-Context</span></span>
<span data-ttu-id="dde0a-116">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="dde0a-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="dde0a-117">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="dde0a-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dde0a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dde0a-118">-DefaultProfile</span></span>
<span data-ttu-id="dde0a-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dde0a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dde0a-120">-Описание</span><span class="sxs-lookup"><span data-stu-id="dde0a-120">-Description</span></span>
<span data-ttu-id="dde0a-121">Описание набора версий API.</span><span class="sxs-lookup"><span data-stu-id="dde0a-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="dde0a-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="dde0a-122">-HeaderName</span></span>
<span data-ttu-id="dde0a-123">Значение заголовка, которое будет содержать сведения о версии.</span><span class="sxs-lookup"><span data-stu-id="dde0a-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="dde0a-124">Если заголовок схемы управления версиями — Choosen, необходимо указать это значение.</span><span class="sxs-lookup"><span data-stu-id="dde0a-124">If versioning Scheme HEADER is choosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="dde0a-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dde0a-125">-InputObject</span></span>
<span data-ttu-id="dde0a-126">Экземпляр PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="dde0a-126">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="dde0a-127">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="dde0a-127">This parameter is required.</span></span>

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

### <span data-ttu-id="dde0a-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dde0a-128">-Name</span></span>
<span data-ttu-id="dde0a-129">Имя набора ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="dde0a-129">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="dde0a-130">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="dde0a-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="dde0a-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dde0a-131">-PassThru</span></span>
<span data-ttu-id="dde0a-132">Если указан, то экземпляр типа Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiVersionSet, который представляет измененный apiVersionSet, будет записываться в Output.</span><span class="sxs-lookup"><span data-stu-id="dde0a-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet type  representing the modified apiVersionSet will be written to output.</span></span>

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

### <span data-ttu-id="dde0a-133">-QueryName</span><span class="sxs-lookup"><span data-stu-id="dde0a-133">-QueryName</span></span>
<span data-ttu-id="dde0a-134">Значение запроса, в котором будут содержаться сведения о версиях.</span><span class="sxs-lookup"><span data-stu-id="dde0a-134">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="dde0a-135">Если запрос на схему управления версиями — Choosen, необходимо указать это значение.</span><span class="sxs-lookup"><span data-stu-id="dde0a-135">If versioning Scheme Query is choosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="dde0a-136">-Схема</span><span class="sxs-lookup"><span data-stu-id="dde0a-136">-Scheme</span></span>
<span data-ttu-id="dde0a-137">Схема управления версиями, которую нужно выбрать для наборов версий API.</span><span class="sxs-lookup"><span data-stu-id="dde0a-137">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="dde0a-138">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="dde0a-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="dde0a-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dde0a-139">-Confirm</span></span>
<span data-ttu-id="dde0a-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dde0a-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dde0a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dde0a-141">-WhatIf</span></span>
<span data-ttu-id="dde0a-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dde0a-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dde0a-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dde0a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dde0a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dde0a-144">CommonParameters</span></span>
<span data-ttu-id="dde0a-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dde0a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dde0a-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dde0a-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dde0a-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dde0a-147">INPUTS</span></span>

### <span data-ttu-id="dde0a-148">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="dde0a-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="dde0a-149">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="dde0a-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>
<span data-ttu-id="dde0a-150">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="dde0a-150">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="dde0a-151">System. String</span><span class="sxs-lookup"><span data-stu-id="dde0a-151">System.String</span></span>

### <span data-ttu-id="dde0a-152">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="dde0a-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="dde0a-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dde0a-153">OUTPUTS</span></span>

### <span data-ttu-id="dde0a-154">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="dde0a-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="dde0a-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="dde0a-155">NOTES</span></span>

## <span data-ttu-id="dde0a-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dde0a-156">RELATED LINKS</span></span>

[<span data-ttu-id="dde0a-157">Get-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="dde0a-157">Get-AzureRmApiManagementApiVersionSet</span></span>](./Get-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="dde0a-158">New-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="dde0a-158">New-AzureRmApiManagementApiVersionSet</span></span>](./New-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="dde0a-159">Set-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="dde0a-159">Set-AzureRmApiManagementApiVersionSet</span></span>](./Set-AzureRmApiManagementApiVersionSet.md)
