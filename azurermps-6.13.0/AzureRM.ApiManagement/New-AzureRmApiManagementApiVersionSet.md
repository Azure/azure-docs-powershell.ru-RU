---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApiVersionSet.md
ms.openlocfilehash: e10b91994bdb7351a7154d04cb7de3231ed87a5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561244"
---
# <span data-ttu-id="62886-101">New-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="62886-101">New-AzureRmApiManagementApiVersionSet</span></span>

## <span data-ttu-id="62886-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="62886-102">SYNOPSIS</span></span>
<span data-ttu-id="62886-103">Создает наборы версий API.</span><span class="sxs-lookup"><span data-stu-id="62886-103">Creates an API Version Set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62886-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="62886-104">SYNTAX</span></span>

```
New-AzureRmApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 -Name <String> -Scheme <PsApiManagementVersioningScheme> [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62886-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62886-105">DESCRIPTION</span></span>
<span data-ttu-id="62886-106">Командлет **New-AzureRmApiManagementApiVersionSet** создает сущность набора версий API в контексте управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="62886-106">The **New-AzureRmApiManagementApiVersionSet** cmdlet creates an API Version set entity in the Azure API Management context.</span></span>

## <span data-ttu-id="62886-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="62886-107">EXAMPLES</span></span>

### <span data-ttu-id="62886-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="62886-108">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> New-AzureRmApiManagementApiVersionSet -Context $ApiMgmtContext  -Name "newversion" -Scheme Header -HeaderName "x-ms-version" -Description "version by xmsversion"

ApiVersionSetId   : ea9a87cd-a699-4a75-bf7d-909846b91268
Description       : version by xmsversion
VersionQueryName  :
VersionHeaderName : x-ms-version
DisplayName       : newversion
VersioningScheme  : Header
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/ea9a87cd-a699-4a75-bf7d-909846b91268
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="62886-109">Эта команда создает версию API, для которой установлена схема управления версиями `Query` и параметр запроса `api-version` .</span><span class="sxs-lookup"><span data-stu-id="62886-109">This command creates an API Version Set which versioning scheme `Query` and Query parameter `api-version`.</span></span>

## <span data-ttu-id="62886-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="62886-110">PARAMETERS</span></span>

### <span data-ttu-id="62886-111">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="62886-111">-ApiVersionSetId</span></span>
<span data-ttu-id="62886-112">Идентификатор для нового множества версий API.</span><span class="sxs-lookup"><span data-stu-id="62886-112">Identifier for new API Version Set.</span></span>
<span data-ttu-id="62886-113">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="62886-113">This parameter is optional.</span></span>
<span data-ttu-id="62886-114">Если не указан, будет создан идентификатор.</span><span class="sxs-lookup"><span data-stu-id="62886-114">If not specified an identifier will be generated.</span></span>

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

### <span data-ttu-id="62886-115">-Context</span><span class="sxs-lookup"><span data-stu-id="62886-115">-Context</span></span>
<span data-ttu-id="62886-116">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="62886-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="62886-117">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="62886-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62886-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62886-118">-DefaultProfile</span></span>
<span data-ttu-id="62886-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="62886-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62886-120">-Описание</span><span class="sxs-lookup"><span data-stu-id="62886-120">-Description</span></span>
<span data-ttu-id="62886-121">Описание набора версий API.</span><span class="sxs-lookup"><span data-stu-id="62886-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="62886-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="62886-122">-HeaderName</span></span>
<span data-ttu-id="62886-123">Значение заголовка, которое будет содержать сведения о версии.</span><span class="sxs-lookup"><span data-stu-id="62886-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="62886-124">Если заголовок схемы управления версиями — Choosen, необходимо указать это значение.</span><span class="sxs-lookup"><span data-stu-id="62886-124">If versioning Scheme HEADER is choosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="62886-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="62886-125">-Name</span></span>
<span data-ttu-id="62886-126">Имя набора ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="62886-126">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="62886-127">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="62886-127">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62886-128">-QueryName</span><span class="sxs-lookup"><span data-stu-id="62886-128">-QueryName</span></span>
<span data-ttu-id="62886-129">Значение запроса, в котором будут содержаться сведения о версиях.</span><span class="sxs-lookup"><span data-stu-id="62886-129">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="62886-130">Если запрос на схему управления версиями — Choosen, необходимо указать это значение.</span><span class="sxs-lookup"><span data-stu-id="62886-130">If versioning Scheme Query is choosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="62886-131">-Схема</span><span class="sxs-lookup"><span data-stu-id="62886-131">-Scheme</span></span>
<span data-ttu-id="62886-132">Схема управления версиями, которую нужно выбрать для наборов версий API.</span><span class="sxs-lookup"><span data-stu-id="62886-132">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="62886-133">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="62886-133">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme
Parameter Sets: (All)
Aliases:
Accepted values: Segment, Query, Header

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62886-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62886-134">-Confirm</span></span>
<span data-ttu-id="62886-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="62886-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62886-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62886-136">-WhatIf</span></span>
<span data-ttu-id="62886-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="62886-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="62886-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="62886-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62886-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62886-139">CommonParameters</span></span>
<span data-ttu-id="62886-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="62886-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62886-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62886-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62886-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="62886-142">INPUTS</span></span>

### <span data-ttu-id="62886-143">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="62886-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>
<span data-ttu-id="62886-144">Параметры: Context (ByValue)</span><span class="sxs-lookup"><span data-stu-id="62886-144">Parameters: Context (ByValue)</span></span>

### <span data-ttu-id="62886-145">System. String</span><span class="sxs-lookup"><span data-stu-id="62886-145">System.String</span></span>

### <span data-ttu-id="62886-146">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="62886-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="62886-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="62886-147">OUTPUTS</span></span>

### <span data-ttu-id="62886-148">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="62886-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="62886-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="62886-149">NOTES</span></span>

## <span data-ttu-id="62886-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62886-150">RELATED LINKS</span></span>

[<span data-ttu-id="62886-151">Get-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="62886-151">Get-AzureRmApiManagementApiVersionSet</span></span>](./Get-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="62886-152">Remove-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="62886-152">Remove-AzureRmApiManagementApiVersionSet</span></span>](./Remove-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="62886-153">Set-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="62886-153">Set-AzureRmApiManagementApiVersionSet</span></span>](./Set-AzureRmApiManagementApiVersionSet.md)
