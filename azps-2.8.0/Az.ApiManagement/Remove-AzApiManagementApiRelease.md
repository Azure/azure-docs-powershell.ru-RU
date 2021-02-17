---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
ms.openlocfilehash: 51a24bcb0951aef7a3feb8b32d3d860d21839ad5
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100407936"
---
# <span data-ttu-id="31bf1-101">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="31bf1-101">Remove-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="31bf1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31bf1-102">SYNOPSIS</span></span>
<span data-ttu-id="31bf1-103">Удаление определенного выпуска API</span><span class="sxs-lookup"><span data-stu-id="31bf1-103">Removes a particular API Release</span></span>

## <span data-ttu-id="31bf1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="31bf1-104">SYNTAX</span></span>

### <span data-ttu-id="31bf1-105">ByApiReleaseId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="31bf1-105">ByApiReleaseId (Default)</span></span>
```
Remove-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ReleaseId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31bf1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="31bf1-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiRelease -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31bf1-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="31bf1-107">DESCRIPTION</span></span>

<span data-ttu-id="31bf1-108">**Cmdlet Remove-AzAzureRmApiManagementApiRelease** удаляет существующий выпуск API.</span><span class="sxs-lookup"><span data-stu-id="31bf1-108">The **Remove-AzAzureRmApiManagementApiRelease** cmdlet removes an existing API Release.</span></span>

## <span data-ttu-id="31bf1-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="31bf1-109">EXAMPLES</span></span>

### <span data-ttu-id="31bf1-110">Пример 1. Удаление выпуска API</span><span class="sxs-lookup"><span data-stu-id="31bf1-110">Example 1: Remove an API Release</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiRelease -Context $apimContext -ApiId "echo-api" -ReleaseId "2"
```

<span data-ttu-id="31bf1-111">Эта команда удаляет выпуск API с указанными ApiId и ReleaseId.</span><span class="sxs-lookup"><span data-stu-id="31bf1-111">This command removes the API Release with the specified ApiId and ReleaseId.</span></span>

## <span data-ttu-id="31bf1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31bf1-112">PARAMETERS</span></span>

### <span data-ttu-id="31bf1-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="31bf1-113">-ApiId</span></span>
<span data-ttu-id="31bf1-114">Идентификатор API.</span><span class="sxs-lookup"><span data-stu-id="31bf1-114">Identifier of the API.</span></span>
<span data-ttu-id="31bf1-115">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="31bf1-115">This parameter is required.</span></span>

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

### <span data-ttu-id="31bf1-116">-Контекст</span><span class="sxs-lookup"><span data-stu-id="31bf1-116">-Context</span></span>
<span data-ttu-id="31bf1-117">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="31bf1-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="31bf1-118">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="31bf1-118">This parameter is required.</span></span>

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

### <span data-ttu-id="31bf1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31bf1-119">-DefaultProfile</span></span>
<span data-ttu-id="31bf1-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="31bf1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31bf1-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31bf1-121">-InputObject</span></span>
<span data-ttu-id="31bf1-122">Экземпляр PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="31bf1-122">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="31bf1-123">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="31bf1-123">This parameter is required.</span></span>

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

### <span data-ttu-id="31bf1-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="31bf1-124">-PassThru</span></span>
<span data-ttu-id="31bf1-125">Если этот задан, будет указано "Истина" в случае успешной операции.</span><span class="sxs-lookup"><span data-stu-id="31bf1-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="31bf1-126">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="31bf1-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="31bf1-127">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="31bf1-127">-ReleaseId</span></span>
<span data-ttu-id="31bf1-128">Идентификатор выпуска API.</span><span class="sxs-lookup"><span data-stu-id="31bf1-128">Identifier of the API Release.</span></span>
<span data-ttu-id="31bf1-129">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="31bf1-129">This parameter is required.</span></span>

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

### <span data-ttu-id="31bf1-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="31bf1-130">-Confirm</span></span>
<span data-ttu-id="31bf1-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="31bf1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31bf1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31bf1-132">-WhatIf</span></span>
<span data-ttu-id="31bf1-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31bf1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31bf1-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="31bf1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31bf1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31bf1-135">CommonParameters</span></span>
<span data-ttu-id="31bf1-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31bf1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31bf1-137">Дополнительные сведения см. [в about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="31bf1-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31bf1-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="31bf1-138">INPUTS</span></span>

### <span data-ttu-id="31bf1-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="31bf1-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="31bf1-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="31bf1-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

### <span data-ttu-id="31bf1-141">System.String</span><span class="sxs-lookup"><span data-stu-id="31bf1-141">System.String</span></span>

## <span data-ttu-id="31bf1-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="31bf1-142">OUTPUTS</span></span>

### <span data-ttu-id="31bf1-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="31bf1-143">System.Boolean</span></span>

## <span data-ttu-id="31bf1-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="31bf1-144">NOTES</span></span>

## <span data-ttu-id="31bf1-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="31bf1-145">RELATED LINKS</span></span>

[<span data-ttu-id="31bf1-146">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="31bf1-146">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="31bf1-147">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="31bf1-147">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)

[<span data-ttu-id="31bf1-148">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="31bf1-148">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)