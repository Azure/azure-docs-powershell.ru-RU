---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
ms.openlocfilehash: 9673df14bdd0f5b7d0e946170a155231e8c4e751
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98423471"
---
# <span data-ttu-id="af55d-101">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="af55d-101">Remove-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="af55d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af55d-102">SYNOPSIS</span></span>
<span data-ttu-id="af55d-103">Удаление определенного выпуска API</span><span class="sxs-lookup"><span data-stu-id="af55d-103">Removes a particular API Release</span></span>

## <span data-ttu-id="af55d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="af55d-104">SYNTAX</span></span>

### <span data-ttu-id="af55d-105">ByApiReleaseId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="af55d-105">ByApiReleaseId (Default)</span></span>
```
Remove-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ReleaseId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af55d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="af55d-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiRelease -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af55d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="af55d-107">DESCRIPTION</span></span>

<span data-ttu-id="af55d-108">Для удаления существующего выпуска API удаляется cmdlet **Remove-AzAzureRmApiManagementApiRelease.**</span><span class="sxs-lookup"><span data-stu-id="af55d-108">The **Remove-AzAzureRmApiManagementApiRelease** cmdlet removes an existing API Release.</span></span>

## <span data-ttu-id="af55d-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="af55d-109">EXAMPLES</span></span>

### <span data-ttu-id="af55d-110">Пример 1. Удаление выпуска API</span><span class="sxs-lookup"><span data-stu-id="af55d-110">Example 1: Remove an API Release</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiRelease -Context $apimContext -ApiId "echo-api" -ReleaseId "2"
```

<span data-ttu-id="af55d-111">Эта команда удаляет выпуск API с указанными ApiId и ReleaseId.</span><span class="sxs-lookup"><span data-stu-id="af55d-111">This command removes the API Release with the specified ApiId and ReleaseId.</span></span>

## <span data-ttu-id="af55d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af55d-112">PARAMETERS</span></span>

### <span data-ttu-id="af55d-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="af55d-113">-ApiId</span></span>
<span data-ttu-id="af55d-114">Идентификатор API.</span><span class="sxs-lookup"><span data-stu-id="af55d-114">Identifier of the API.</span></span>
<span data-ttu-id="af55d-115">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="af55d-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af55d-116">-Контекст</span><span class="sxs-lookup"><span data-stu-id="af55d-116">-Context</span></span>
<span data-ttu-id="af55d-117">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="af55d-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="af55d-118">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="af55d-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af55d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af55d-119">-DefaultProfile</span></span>
<span data-ttu-id="af55d-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="af55d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af55d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af55d-121">-InputObject</span></span>
<span data-ttu-id="af55d-122">Экземпляр PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="af55d-122">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="af55d-123">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="af55d-123">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af55d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="af55d-124">-PassThru</span></span>
<span data-ttu-id="af55d-125">Если этот задан, будет указано "Истина" в случае успешной операции.</span><span class="sxs-lookup"><span data-stu-id="af55d-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="af55d-126">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="af55d-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="af55d-127">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="af55d-127">-ReleaseId</span></span>
<span data-ttu-id="af55d-128">Идентификатор выпуска API.</span><span class="sxs-lookup"><span data-stu-id="af55d-128">Identifier of the API Release.</span></span>
<span data-ttu-id="af55d-129">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="af55d-129">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af55d-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af55d-130">-Confirm</span></span>
<span data-ttu-id="af55d-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af55d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af55d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af55d-132">-WhatIf</span></span>
<span data-ttu-id="af55d-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af55d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af55d-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="af55d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af55d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af55d-135">CommonParameters</span></span>
<span data-ttu-id="af55d-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af55d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af55d-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="af55d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af55d-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="af55d-138">INPUTS</span></span>

### <span data-ttu-id="af55d-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="af55d-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="af55d-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="af55d-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

### <span data-ttu-id="af55d-141">System.String</span><span class="sxs-lookup"><span data-stu-id="af55d-141">System.String</span></span>

## <span data-ttu-id="af55d-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="af55d-142">OUTPUTS</span></span>

### <span data-ttu-id="af55d-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="af55d-143">System.Boolean</span></span>

## <span data-ttu-id="af55d-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="af55d-144">NOTES</span></span>

## <span data-ttu-id="af55d-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="af55d-145">RELATED LINKS</span></span>

[<span data-ttu-id="af55d-146">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="af55d-146">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="af55d-147">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="af55d-147">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)

[<span data-ttu-id="af55d-148">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="af55d-148">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)