---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementApiRelease.md
ms.openlocfilehash: 99ec1234eea582fb91f2722032cb23c27e86b878
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402948"
---
# <span data-ttu-id="61ddb-101">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="61ddb-101">Update-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="61ddb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61ddb-102">SYNOPSIS</span></span>
<span data-ttu-id="61ddb-103">Обновляет определенный выпуск API.</span><span class="sxs-lookup"><span data-stu-id="61ddb-103">Updates a particular Api Release.</span></span>

## <span data-ttu-id="61ddb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="61ddb-104">SYNTAX</span></span>

### <span data-ttu-id="61ddb-105">ExpandedParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="61ddb-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementApiRelease -Context <PsApiManagementContext> -ReleaseId <String> -ApiId <String>
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="61ddb-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="61ddb-106">ByInputObject</span></span>
```
Update-AzApiManagementApiRelease [-Note <String>] -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61ddb-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="61ddb-107">DESCRIPTION</span></span>
<span data-ttu-id="61ddb-108">Cmdlet **Update-AzApiManagementApiRelease** изменяет выпуск API управления Azure API.</span><span class="sxs-lookup"><span data-stu-id="61ddb-108">The **Update-AzApiManagementApiRelease** cmdlet modifies an Azure API Management API Release.</span></span>

## <span data-ttu-id="61ddb-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="61ddb-109">EXAMPLES</span></span>

### <span data-ttu-id="61ddb-110">Пример 1. Обновление выпуска API для изменения его редакции</span><span class="sxs-lookup"><span data-stu-id="61ddb-110">Example 1: Updates an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId "echo-api" -ReleaseId "echo-api-release" -Note "Releasing version 2 of the echo-api to public"
```

<span data-ttu-id="61ddb-111">Эта команда обновляет выпуск API для `echo-api-release` API с новой `echo-api` заметкой.</span><span class="sxs-lookup"><span data-stu-id="61ddb-111">This command updates the `echo-api-release` API Release of the Api `echo-api` with new note.</span></span>

## <span data-ttu-id="61ddb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61ddb-112">PARAMETERS</span></span>

### <span data-ttu-id="61ddb-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="61ddb-113">-ApiId</span></span>
<span data-ttu-id="61ddb-114">Идентификатор существующего API.</span><span class="sxs-lookup"><span data-stu-id="61ddb-114">Identifier of existing API.</span></span>
<span data-ttu-id="61ddb-115">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="61ddb-115">This parameter is required.</span></span>

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

### <span data-ttu-id="61ddb-116">-Контекст</span><span class="sxs-lookup"><span data-stu-id="61ddb-116">-Context</span></span>
<span data-ttu-id="61ddb-117">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="61ddb-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="61ddb-118">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="61ddb-118">This parameter is required.</span></span>

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

### <span data-ttu-id="61ddb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61ddb-119">-DefaultProfile</span></span>
<span data-ttu-id="61ddb-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="61ddb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61ddb-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61ddb-121">-InputObject</span></span>
<span data-ttu-id="61ddb-122">Экземпляр типа Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="61ddb-122">Instance of type Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease.</span></span>

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

### <span data-ttu-id="61ddb-123">-Note</span><span class="sxs-lookup"><span data-stu-id="61ddb-123">-Note</span></span>
<span data-ttu-id="61ddb-124">Заметки о выпуске Api.</span><span class="sxs-lookup"><span data-stu-id="61ddb-124">Api Release Notes.</span></span>
<span data-ttu-id="61ddb-125">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="61ddb-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="61ddb-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="61ddb-126">-PassThru</span></span>
<span data-ttu-id="61ddb-127">Экземпляр Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease, представляющий выпуск API набора.</span><span class="sxs-lookup"><span data-stu-id="61ddb-127">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease type representing the set API Release.</span></span>

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

### <span data-ttu-id="61ddb-128">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="61ddb-128">-ReleaseId</span></span>
<span data-ttu-id="61ddb-129">Идентификатор для Api Revision ReleaseId.</span><span class="sxs-lookup"><span data-stu-id="61ddb-129">Identifier for the Api Revision ReleaseId.</span></span>
<span data-ttu-id="61ddb-130">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="61ddb-130">This parameter is required.</span></span>

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

### <span data-ttu-id="61ddb-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61ddb-131">-Confirm</span></span>
<span data-ttu-id="61ddb-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61ddb-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61ddb-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61ddb-133">-WhatIf</span></span>
<span data-ttu-id="61ddb-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61ddb-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61ddb-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="61ddb-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61ddb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61ddb-136">CommonParameters</span></span>
<span data-ttu-id="61ddb-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61ddb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61ddb-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="61ddb-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61ddb-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="61ddb-139">INPUTS</span></span>

### <span data-ttu-id="61ddb-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="61ddb-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="61ddb-141">System.String</span><span class="sxs-lookup"><span data-stu-id="61ddb-141">System.String</span></span>

### <span data-ttu-id="61ddb-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="61ddb-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="61ddb-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="61ddb-143">OUTPUTS</span></span>

### <span data-ttu-id="61ddb-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="61ddb-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="61ddb-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="61ddb-145">NOTES</span></span>

## <span data-ttu-id="61ddb-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="61ddb-146">RELATED LINKS</span></span>

[<span data-ttu-id="61ddb-147">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="61ddb-147">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="61ddb-148">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="61ddb-148">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)
