---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 8cbb9afc37242330bc76b7413033dc41cbd61cd4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973000"
---
# <span data-ttu-id="7f105-101">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="7f105-101">Remove-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="7f105-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f105-102">SYNOPSIS</span></span>
<span data-ttu-id="7f105-103">Удаляет сервер авторизации.</span><span class="sxs-lookup"><span data-stu-id="7f105-103">Removes an authorization server.</span></span>

## <span data-ttu-id="7f105-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7f105-104">SYNTAX</span></span>

```
Remove-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f105-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f105-105">DESCRIPTION</span></span>
<span data-ttu-id="7f105-106">Из-за выполнения **cmdlet Remove-AzApiManagementAuthorizationServer** удаляется сервер авторизации управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="7f105-106">The **Remove-AzApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="7f105-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7f105-107">EXAMPLES</span></span>

### <span data-ttu-id="7f105-108">Пример 1. Удаление сервера авторизации</span><span class="sxs-lookup"><span data-stu-id="7f105-108">Example 1: Remove an authorization server</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId "authserverid" -Force
```

<span data-ttu-id="7f105-109">Эта команда удаляет указанный сервер авторизации управления API.</span><span class="sxs-lookup"><span data-stu-id="7f105-109">This command removes the specified API Management Authorization Server.</span></span>
<span data-ttu-id="7f105-110">Так как *параметр Force* указан, подтверждение не требуется.</span><span class="sxs-lookup"><span data-stu-id="7f105-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="7f105-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f105-111">PARAMETERS</span></span>

### <span data-ttu-id="7f105-112">-Контекст</span><span class="sxs-lookup"><span data-stu-id="7f105-112">-Context</span></span>
<span data-ttu-id="7f105-113">Указывает объект **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="7f105-113">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="7f105-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f105-114">-DefaultProfile</span></span>
<span data-ttu-id="7f105-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7f105-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f105-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7f105-116">-PassThru</span></span>
<span data-ttu-id="7f105-117">passthru</span><span class="sxs-lookup"><span data-stu-id="7f105-117">passthru</span></span>

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

### <span data-ttu-id="7f105-118">-ServerId</span><span class="sxs-lookup"><span data-stu-id="7f105-118">-ServerId</span></span>
<span data-ttu-id="7f105-119">Определяет ID сервера авторизации, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="7f105-119">Specifies the ID of the authorization server to remove.</span></span>

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

### <span data-ttu-id="7f105-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7f105-120">-Confirm</span></span>
<span data-ttu-id="7f105-121">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f105-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f105-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f105-122">-WhatIf</span></span>
<span data-ttu-id="7f105-123">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f105-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f105-124">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7f105-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f105-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f105-125">CommonParameters</span></span>
<span data-ttu-id="7f105-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f105-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f105-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f105-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f105-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7f105-128">INPUTS</span></span>

### <span data-ttu-id="7f105-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7f105-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7f105-130">System.String</span><span class="sxs-lookup"><span data-stu-id="7f105-130">System.String</span></span>

### <span data-ttu-id="7f105-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7f105-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7f105-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7f105-132">OUTPUTS</span></span>

### <span data-ttu-id="7f105-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7f105-133">System.Boolean</span></span>

## <span data-ttu-id="7f105-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7f105-134">NOTES</span></span>

## <span data-ttu-id="7f105-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7f105-135">RELATED LINKS</span></span>

[<span data-ttu-id="7f105-136">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="7f105-136">Get-AzApiManagementAuthorizationServer</span></span>](./Get-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="7f105-137">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="7f105-137">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="7f105-138">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="7f105-138">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


