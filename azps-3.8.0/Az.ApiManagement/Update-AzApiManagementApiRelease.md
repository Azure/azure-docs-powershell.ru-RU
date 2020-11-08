---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementApiRelease.md
ms.openlocfilehash: 99ec1234eea582fb91f2722032cb23c27e86b878
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074162"
---
# <span data-ttu-id="3be7d-101">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="3be7d-101">Update-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="3be7d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3be7d-102">SYNOPSIS</span></span>
<span data-ttu-id="3be7d-103">Обновляет определенный выпуск API.</span><span class="sxs-lookup"><span data-stu-id="3be7d-103">Updates a particular Api Release.</span></span>

## <span data-ttu-id="3be7d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3be7d-104">SYNTAX</span></span>

### <span data-ttu-id="3be7d-105">ExpandedParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3be7d-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementApiRelease -Context <PsApiManagementContext> -ReleaseId <String> -ApiId <String>
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3be7d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3be7d-106">ByInputObject</span></span>
```
Update-AzApiManagementApiRelease [-Note <String>] -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3be7d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3be7d-107">DESCRIPTION</span></span>
<span data-ttu-id="3be7d-108">Командлет **Update-AzApiManagementApiRelease** изменяет выпускную функцию API для управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="3be7d-108">The **Update-AzApiManagementApiRelease** cmdlet modifies an Azure API Management API Release.</span></span>

## <span data-ttu-id="3be7d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3be7d-109">EXAMPLES</span></span>

### <span data-ttu-id="3be7d-110">Пример 1: Обновление выпусков API для редакции API</span><span class="sxs-lookup"><span data-stu-id="3be7d-110">Example 1: Updates an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId "echo-api" -ReleaseId "echo-api-release" -Note "Releasing version 2 of the echo-api to public"
```

<span data-ttu-id="3be7d-111">Эта команда обновляет `echo-api-release` выпуски API API `echo-api` с новой заметкой.</span><span class="sxs-lookup"><span data-stu-id="3be7d-111">This command updates the `echo-api-release` API Release of the Api `echo-api` with new note.</span></span>

## <span data-ttu-id="3be7d-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3be7d-112">PARAMETERS</span></span>

### <span data-ttu-id="3be7d-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="3be7d-113">-ApiId</span></span>
<span data-ttu-id="3be7d-114">Идентификатор существующего API.</span><span class="sxs-lookup"><span data-stu-id="3be7d-114">Identifier of existing API.</span></span>
<span data-ttu-id="3be7d-115">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="3be7d-115">This parameter is required.</span></span>

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

### <span data-ttu-id="3be7d-116">-Context</span><span class="sxs-lookup"><span data-stu-id="3be7d-116">-Context</span></span>
<span data-ttu-id="3be7d-117">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="3be7d-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="3be7d-118">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="3be7d-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3be7d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3be7d-119">-DefaultProfile</span></span>
<span data-ttu-id="3be7d-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3be7d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3be7d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3be7d-121">-InputObject</span></span>
<span data-ttu-id="3be7d-122">Экземпляр типа Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="3be7d-122">Instance of type Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3be7d-123">-Примечание</span><span class="sxs-lookup"><span data-stu-id="3be7d-123">-Note</span></span>
<span data-ttu-id="3be7d-124">Заметки о выпуске API.</span><span class="sxs-lookup"><span data-stu-id="3be7d-124">Api Release Notes.</span></span>
<span data-ttu-id="3be7d-125">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="3be7d-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="3be7d-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3be7d-126">-PassThru</span></span>
<span data-ttu-id="3be7d-127">Если указан экземпляр Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease, представляющий выпуск API набора.</span><span class="sxs-lookup"><span data-stu-id="3be7d-127">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease type representing the set API Release.</span></span>

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

### <span data-ttu-id="3be7d-128">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="3be7d-128">-ReleaseId</span></span>
<span data-ttu-id="3be7d-129">Идентификатор для API редакции ReleaseId.</span><span class="sxs-lookup"><span data-stu-id="3be7d-129">Identifier for the Api Revision ReleaseId.</span></span>
<span data-ttu-id="3be7d-130">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="3be7d-130">This parameter is required.</span></span>

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

### <span data-ttu-id="3be7d-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3be7d-131">-Confirm</span></span>
<span data-ttu-id="3be7d-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3be7d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3be7d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3be7d-133">-WhatIf</span></span>
<span data-ttu-id="3be7d-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3be7d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3be7d-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3be7d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3be7d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3be7d-136">CommonParameters</span></span>
<span data-ttu-id="3be7d-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3be7d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3be7d-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3be7d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3be7d-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3be7d-139">INPUTS</span></span>

### <span data-ttu-id="3be7d-140">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3be7d-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3be7d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="3be7d-141">System.String</span></span>

### <span data-ttu-id="3be7d-142">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="3be7d-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="3be7d-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3be7d-143">OUTPUTS</span></span>

### <span data-ttu-id="3be7d-144">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="3be7d-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="3be7d-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="3be7d-145">NOTES</span></span>

## <span data-ttu-id="3be7d-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3be7d-146">RELATED LINKS</span></span>

[<span data-ttu-id="3be7d-147">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="3be7d-147">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="3be7d-148">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="3be7d-148">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)
