---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
ms.openlocfilehash: 9673df14bdd0f5b7d0e946170a155231e8c4e751
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412662"
---
# <span data-ttu-id="04f75-101">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="04f75-101">Remove-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="04f75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04f75-102">SYNOPSIS</span></span>
<span data-ttu-id="04f75-103">Удаление определенного выпуска API</span><span class="sxs-lookup"><span data-stu-id="04f75-103">Removes a particular API Release</span></span>

## <span data-ttu-id="04f75-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="04f75-104">SYNTAX</span></span>

### <span data-ttu-id="04f75-105">ByApiReleaseId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="04f75-105">ByApiReleaseId (Default)</span></span>
```
Remove-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ReleaseId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04f75-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="04f75-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiRelease -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04f75-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="04f75-107">DESCRIPTION</span></span>

<span data-ttu-id="04f75-108">**Cmdlet Remove-AzAzureRmApiManagementApiRelease** удаляет существующий выпуск API.</span><span class="sxs-lookup"><span data-stu-id="04f75-108">The **Remove-AzAzureRmApiManagementApiRelease** cmdlet removes an existing API Release.</span></span>

## <span data-ttu-id="04f75-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="04f75-109">EXAMPLES</span></span>

### <span data-ttu-id="04f75-110">Пример 1. Удаление выпуска API</span><span class="sxs-lookup"><span data-stu-id="04f75-110">Example 1: Remove an API Release</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiRelease -Context $apimContext -ApiId "echo-api" -ReleaseId "2"
```

<span data-ttu-id="04f75-111">Эта команда удаляет выпуск API с указанными ApiId и ReleaseId.</span><span class="sxs-lookup"><span data-stu-id="04f75-111">This command removes the API Release with the specified ApiId and ReleaseId.</span></span>

## <span data-ttu-id="04f75-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04f75-112">PARAMETERS</span></span>

### <span data-ttu-id="04f75-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="04f75-113">-ApiId</span></span>
<span data-ttu-id="04f75-114">Идентификатор API.</span><span class="sxs-lookup"><span data-stu-id="04f75-114">Identifier of the API.</span></span>
<span data-ttu-id="04f75-115">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="04f75-115">This parameter is required.</span></span>

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

### <span data-ttu-id="04f75-116">-Контекст</span><span class="sxs-lookup"><span data-stu-id="04f75-116">-Context</span></span>
<span data-ttu-id="04f75-117">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="04f75-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="04f75-118">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="04f75-118">This parameter is required.</span></span>

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

### <span data-ttu-id="04f75-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04f75-119">-DefaultProfile</span></span>
<span data-ttu-id="04f75-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="04f75-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04f75-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04f75-121">-InputObject</span></span>
<span data-ttu-id="04f75-122">Экземпляр PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="04f75-122">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="04f75-123">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="04f75-123">This parameter is required.</span></span>

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

### <span data-ttu-id="04f75-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04f75-124">-PassThru</span></span>
<span data-ttu-id="04f75-125">Если этот задан, будет указано "Истина" в случае успешной операции.</span><span class="sxs-lookup"><span data-stu-id="04f75-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="04f75-126">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="04f75-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="04f75-127">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="04f75-127">-ReleaseId</span></span>
<span data-ttu-id="04f75-128">Идентификатор выпуска API.</span><span class="sxs-lookup"><span data-stu-id="04f75-128">Identifier of the API Release.</span></span>
<span data-ttu-id="04f75-129">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="04f75-129">This parameter is required.</span></span>

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

### <span data-ttu-id="04f75-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="04f75-130">-Confirm</span></span>
<span data-ttu-id="04f75-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="04f75-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04f75-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04f75-132">-WhatIf</span></span>
<span data-ttu-id="04f75-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04f75-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04f75-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="04f75-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04f75-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04f75-135">CommonParameters</span></span>
<span data-ttu-id="04f75-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04f75-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04f75-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="04f75-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04f75-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="04f75-138">INPUTS</span></span>

### <span data-ttu-id="04f75-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="04f75-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="04f75-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="04f75-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

### <span data-ttu-id="04f75-141">System.String</span><span class="sxs-lookup"><span data-stu-id="04f75-141">System.String</span></span>

## <span data-ttu-id="04f75-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="04f75-142">OUTPUTS</span></span>

### <span data-ttu-id="04f75-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="04f75-143">System.Boolean</span></span>

## <span data-ttu-id="04f75-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="04f75-144">NOTES</span></span>

## <span data-ttu-id="04f75-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="04f75-145">RELATED LINKS</span></span>

[<span data-ttu-id="04f75-146">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="04f75-146">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="04f75-147">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="04f75-147">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)

[<span data-ttu-id="04f75-148">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="04f75-148">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)