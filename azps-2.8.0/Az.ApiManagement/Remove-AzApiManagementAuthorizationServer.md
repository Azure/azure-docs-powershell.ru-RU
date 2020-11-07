---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 41266c660a7dde6064b7f57e3f0303359bba6a8e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728001"
---
# <span data-ttu-id="dc2ac-101">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="dc2ac-101">Remove-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="dc2ac-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dc2ac-102">SYNOPSIS</span></span>
<span data-ttu-id="dc2ac-103">Удаление сервера авторизации.</span><span class="sxs-lookup"><span data-stu-id="dc2ac-103">Removes an authorization server.</span></span>

## <span data-ttu-id="dc2ac-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dc2ac-104">SYNTAX</span></span>

```
Remove-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc2ac-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc2ac-105">DESCRIPTION</span></span>
<span data-ttu-id="dc2ac-106">Командлет **Remove-AzApiManagementAuthorizationServer** удаляет сервер авторизации управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="dc2ac-106">The **Remove-AzApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="dc2ac-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dc2ac-107">EXAMPLES</span></span>

### <span data-ttu-id="dc2ac-108">Пример 1: Удаление сервера авторизации</span><span class="sxs-lookup"><span data-stu-id="dc2ac-108">Example 1: Remove an authorization server</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId "authserverid" -Force
```

<span data-ttu-id="dc2ac-109">Эта команда удаляет указанный сервер авторизации управления API.</span><span class="sxs-lookup"><span data-stu-id="dc2ac-109">This command removes the specified API Management Authorization Server.</span></span>
<span data-ttu-id="dc2ac-110">Так как указан параметр *Force* , подтверждение не требуется.</span><span class="sxs-lookup"><span data-stu-id="dc2ac-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="dc2ac-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dc2ac-111">PARAMETERS</span></span>

### <span data-ttu-id="dc2ac-112">-Context</span><span class="sxs-lookup"><span data-stu-id="dc2ac-112">-Context</span></span>
<span data-ttu-id="dc2ac-113">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="dc2ac-113">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="dc2ac-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc2ac-114">-DefaultProfile</span></span>
<span data-ttu-id="dc2ac-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dc2ac-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc2ac-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc2ac-116">-PassThru</span></span>
<span data-ttu-id="dc2ac-117">PassThru</span><span class="sxs-lookup"><span data-stu-id="dc2ac-117">passthru</span></span>

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

### <span data-ttu-id="dc2ac-118">-ServerId</span><span class="sxs-lookup"><span data-stu-id="dc2ac-118">-ServerId</span></span>
<span data-ttu-id="dc2ac-119">Указывает идентификатор сервера авторизации, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="dc2ac-119">Specifies the ID of the authorization server to remove.</span></span>

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

### <span data-ttu-id="dc2ac-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc2ac-120">-Confirm</span></span>
<span data-ttu-id="dc2ac-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dc2ac-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc2ac-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc2ac-122">-WhatIf</span></span>
<span data-ttu-id="dc2ac-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dc2ac-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc2ac-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dc2ac-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc2ac-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc2ac-125">CommonParameters</span></span>
<span data-ttu-id="dc2ac-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dc2ac-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc2ac-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc2ac-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc2ac-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dc2ac-128">INPUTS</span></span>

### <span data-ttu-id="dc2ac-129">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="dc2ac-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="dc2ac-130">System. String</span><span class="sxs-lookup"><span data-stu-id="dc2ac-130">System.String</span></span>

### <span data-ttu-id="dc2ac-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="dc2ac-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="dc2ac-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc2ac-132">OUTPUTS</span></span>

### <span data-ttu-id="dc2ac-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dc2ac-133">System.Boolean</span></span>

## <span data-ttu-id="dc2ac-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="dc2ac-134">NOTES</span></span>

## <span data-ttu-id="dc2ac-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc2ac-135">RELATED LINKS</span></span>

[<span data-ttu-id="dc2ac-136">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="dc2ac-136">Get-AzApiManagementAuthorizationServer</span></span>](./Get-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="dc2ac-137">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="dc2ac-137">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="dc2ac-138">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="dc2ac-138">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


