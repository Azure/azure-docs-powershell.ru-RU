---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F23D9274-63B9-4654-897B-6E84757774D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
ms.openlocfilehash: 13f5297efc19aa56cc5af55962c072f5ff2a32d0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98423511"
---
# <span data-ttu-id="1d8ed-101">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1d8ed-101">Remove-AzApiManagementApi</span></span>

## <span data-ttu-id="1d8ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d8ed-102">SYNOPSIS</span></span>
<span data-ttu-id="1d8ed-103">Удаляет API.</span><span class="sxs-lookup"><span data-stu-id="1d8ed-103">Removes an API.</span></span>

## <span data-ttu-id="1d8ed-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1d8ed-104">SYNTAX</span></span>

```
Remove-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d8ed-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d8ed-105">DESCRIPTION</span></span>
<span data-ttu-id="1d8ed-106">Для удаления существующего API **удаляется cmdlet Remove-AzApiManagementApi.**</span><span class="sxs-lookup"><span data-stu-id="1d8ed-106">The **Remove-AzApiManagementApi** cmdlet removes an existing API.</span></span>

## <span data-ttu-id="1d8ed-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1d8ed-107">EXAMPLES</span></span>

### <span data-ttu-id="1d8ed-108">Пример 1. Удаление API</span><span class="sxs-lookup"><span data-stu-id="1d8ed-108">Example 1: Remove an API</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApi -Context $apimContext -ApiId "0123456789"
```

<span data-ttu-id="1d8ed-109">Эта команда удаляет API с указанным ИД.</span><span class="sxs-lookup"><span data-stu-id="1d8ed-109">This command removes the API with the specified ID.</span></span>

## <span data-ttu-id="1d8ed-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d8ed-110">PARAMETERS</span></span>

### <span data-ttu-id="1d8ed-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="1d8ed-111">-ApiId</span></span>
<span data-ttu-id="1d8ed-112">Определяет ИД удаления API.</span><span class="sxs-lookup"><span data-stu-id="1d8ed-112">Specifies the ID of the API remove.</span></span>

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

### <span data-ttu-id="1d8ed-113">-Контекст</span><span class="sxs-lookup"><span data-stu-id="1d8ed-113">-Context</span></span>
<span data-ttu-id="1d8ed-114">Указывает объект **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="1d8ed-114">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d8ed-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d8ed-115">-DefaultProfile</span></span>
<span data-ttu-id="1d8ed-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1d8ed-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d8ed-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1d8ed-117">-PassThru</span></span>
<span data-ttu-id="1d8ed-118">passthru</span><span class="sxs-lookup"><span data-stu-id="1d8ed-118">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d8ed-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1d8ed-119">-Confirm</span></span>
<span data-ttu-id="1d8ed-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d8ed-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d8ed-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d8ed-121">-WhatIf</span></span>
<span data-ttu-id="1d8ed-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d8ed-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d8ed-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1d8ed-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d8ed-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d8ed-124">CommonParameters</span></span>
<span data-ttu-id="1d8ed-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d8ed-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d8ed-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1d8ed-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d8ed-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1d8ed-127">INPUTS</span></span>

### <span data-ttu-id="1d8ed-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1d8ed-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1d8ed-129">System.String</span><span class="sxs-lookup"><span data-stu-id="1d8ed-129">System.String</span></span>

### <span data-ttu-id="1d8ed-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1d8ed-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1d8ed-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1d8ed-131">OUTPUTS</span></span>

### <span data-ttu-id="1d8ed-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1d8ed-132">System.Boolean</span></span>

## <span data-ttu-id="1d8ed-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1d8ed-133">NOTES</span></span>

## <span data-ttu-id="1d8ed-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1d8ed-134">RELATED LINKS</span></span>

[<span data-ttu-id="1d8ed-135">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1d8ed-135">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="1d8ed-136">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1d8ed-136">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="1d8ed-137">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1d8ed-137">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="1d8ed-138">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1d8ed-138">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="1d8ed-139">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1d8ed-139">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


