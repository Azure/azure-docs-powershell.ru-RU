---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 0e007634659d842b0c59712a2ee191a79e1aeb58
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079894"
---
# <span data-ttu-id="bced4-101">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="bced4-101">New-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="bced4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bced4-102">SYNOPSIS</span></span>
<span data-ttu-id="bced4-103">Создает наборы версий API.</span><span class="sxs-lookup"><span data-stu-id="bced4-103">Creates an API Version Set.</span></span>

## <span data-ttu-id="bced4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bced4-104">SYNTAX</span></span>

```
New-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>] -Name <String>
 -Scheme <PsApiManagementVersioningScheme> [-HeaderName <String>] [-QueryName <String>] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bced4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bced4-105">DESCRIPTION</span></span>
<span data-ttu-id="bced4-106">Командлет **New-AzApiManagementApiVersionSet** создает сущность набора версий API в контексте управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="bced4-106">The **New-AzApiManagementApiVersionSet** cmdlet creates an API Version set entity in the Azure API Management context.</span></span>

## <span data-ttu-id="bced4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bced4-107">EXAMPLES</span></span>

### <span data-ttu-id="bced4-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bced4-108">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> New-AzApiManagementApiVersionSet -Context $ApiMgmtContext  -Name "newversion" -Scheme Header -HeaderName "x-ms-version" -Description "version by xmsversion"

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

<span data-ttu-id="bced4-109">Эта команда создает версию API, для которой установлена схема управления версиями `Query` и параметр запроса `api-version` .</span><span class="sxs-lookup"><span data-stu-id="bced4-109">This command creates an API Version Set which versioning scheme `Query` and Query parameter `api-version`.</span></span>

## <span data-ttu-id="bced4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bced4-110">PARAMETERS</span></span>

### <span data-ttu-id="bced4-111">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="bced4-111">-ApiVersionSetId</span></span>
<span data-ttu-id="bced4-112">Идентификатор для нового множества версий API.</span><span class="sxs-lookup"><span data-stu-id="bced4-112">Identifier for new API Version Set.</span></span>
<span data-ttu-id="bced4-113">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="bced4-113">This parameter is optional.</span></span>
<span data-ttu-id="bced4-114">Если не указан, будет создан идентификатор.</span><span class="sxs-lookup"><span data-stu-id="bced4-114">If not specified an identifier will be generated.</span></span>

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

### <span data-ttu-id="bced4-115">-Context</span><span class="sxs-lookup"><span data-stu-id="bced4-115">-Context</span></span>
<span data-ttu-id="bced4-116">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="bced4-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="bced4-117">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="bced4-117">This parameter is required.</span></span>

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

### <span data-ttu-id="bced4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bced4-118">-DefaultProfile</span></span>
<span data-ttu-id="bced4-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bced4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bced4-120">-Описание</span><span class="sxs-lookup"><span data-stu-id="bced4-120">-Description</span></span>
<span data-ttu-id="bced4-121">Описание набора версий API.</span><span class="sxs-lookup"><span data-stu-id="bced4-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="bced4-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="bced4-122">-HeaderName</span></span>
<span data-ttu-id="bced4-123">Значение заголовка, которое будет содержать сведения о версии.</span><span class="sxs-lookup"><span data-stu-id="bced4-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="bced4-124">Если выбран заголовок схема управления версиями, необходимо указать это значение.</span><span class="sxs-lookup"><span data-stu-id="bced4-124">If versioning Scheme HEADER is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="bced4-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bced4-125">-Name</span></span>
<span data-ttu-id="bced4-126">Имя набора ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="bced4-126">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="bced4-127">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="bced4-127">This parameter is required.</span></span>

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

### <span data-ttu-id="bced4-128">-QueryName</span><span class="sxs-lookup"><span data-stu-id="bced4-128">-QueryName</span></span>
<span data-ttu-id="bced4-129">Значение запроса, в котором будут содержаться сведения о версиях.</span><span class="sxs-lookup"><span data-stu-id="bced4-129">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="bced4-130">Если выбран запрос на схему управления версиями, необходимо указать это значение.</span><span class="sxs-lookup"><span data-stu-id="bced4-130">If versioning Scheme Query is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="bced4-131">-Схема</span><span class="sxs-lookup"><span data-stu-id="bced4-131">-Scheme</span></span>
<span data-ttu-id="bced4-132">Схема управления версиями, которую нужно выбрать для наборов версий API.</span><span class="sxs-lookup"><span data-stu-id="bced4-132">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="bced4-133">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="bced4-133">This parameter is required.</span></span>

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

### <span data-ttu-id="bced4-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bced4-134">-Confirm</span></span>
<span data-ttu-id="bced4-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bced4-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bced4-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bced4-136">-WhatIf</span></span>
<span data-ttu-id="bced4-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bced4-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bced4-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bced4-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bced4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bced4-139">CommonParameters</span></span>
<span data-ttu-id="bced4-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bced4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bced4-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bced4-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bced4-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bced4-142">INPUTS</span></span>

### <span data-ttu-id="bced4-143">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bced4-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bced4-144">System. String</span><span class="sxs-lookup"><span data-stu-id="bced4-144">System.String</span></span>

### <span data-ttu-id="bced4-145">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="bced4-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="bced4-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bced4-146">OUTPUTS</span></span>

### <span data-ttu-id="bced4-147">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="bced4-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="bced4-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="bced4-148">NOTES</span></span>

## <span data-ttu-id="bced4-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bced4-149">RELATED LINKS</span></span>

[<span data-ttu-id="bced4-150">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="bced4-150">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="bced4-151">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="bced4-151">Remove-AzApiManagementApiVersionSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="bced4-152">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="bced4-152">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)