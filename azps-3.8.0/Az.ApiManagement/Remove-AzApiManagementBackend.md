---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
ms.openlocfilehash: 073b32936be1e1614e495ca680a250498742ba66
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100414600"
---
# <span data-ttu-id="c71f6-101">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="c71f6-101">Remove-AzApiManagementBackend</span></span>

## <span data-ttu-id="c71f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c71f6-102">SYNOPSIS</span></span>
<span data-ttu-id="c71f6-103">Удаляет "Backend".</span><span class="sxs-lookup"><span data-stu-id="c71f6-103">Removes a Backend.</span></span>

## <span data-ttu-id="c71f6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c71f6-104">SYNTAX</span></span>

```
Remove-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c71f6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c71f6-105">DESCRIPTION</span></span>
<span data-ttu-id="c71f6-106">Из управления Api удаляется заданный идентификатором.</span><span class="sxs-lookup"><span data-stu-id="c71f6-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="c71f6-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c71f6-107">EXAMPLES</span></span>

### <span data-ttu-id="c71f6-108">Пример 1. Удаление backend 123</span><span class="sxs-lookup"><span data-stu-id="c71f6-108">Example 1: Remove the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="c71f6-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c71f6-109">PARAMETERS</span></span>

### <span data-ttu-id="c71f6-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="c71f6-110">-BackendId</span></span>
<span data-ttu-id="c71f6-111">Идентификатор существующего backend.</span><span class="sxs-lookup"><span data-stu-id="c71f6-111">Identifier of existing backend.</span></span>
<span data-ttu-id="c71f6-112">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="c71f6-112">This parameter is required.</span></span>

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

### <span data-ttu-id="c71f6-113">-Контекст</span><span class="sxs-lookup"><span data-stu-id="c71f6-113">-Context</span></span>
<span data-ttu-id="c71f6-114">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c71f6-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c71f6-115">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="c71f6-115">This parameter is required.</span></span>

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

### <span data-ttu-id="c71f6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c71f6-116">-DefaultProfile</span></span>
<span data-ttu-id="c71f6-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c71f6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c71f6-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c71f6-118">-PassThru</span></span>
<span data-ttu-id="c71f6-119">Если этот задан, будет указано "Истина" в случае успешной операции.</span><span class="sxs-lookup"><span data-stu-id="c71f6-119">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="c71f6-120">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c71f6-120">This parameter is optional.</span></span>
<span data-ttu-id="c71f6-121">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="c71f6-121">Default value is false.</span></span>

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

### <span data-ttu-id="c71f6-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c71f6-122">-Confirm</span></span>
<span data-ttu-id="c71f6-123">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="c71f6-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c71f6-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c71f6-124">-WhatIf</span></span>
<span data-ttu-id="c71f6-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c71f6-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c71f6-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c71f6-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c71f6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c71f6-127">CommonParameters</span></span>
<span data-ttu-id="c71f6-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c71f6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c71f6-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c71f6-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c71f6-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c71f6-130">INPUTS</span></span>

### <span data-ttu-id="c71f6-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c71f6-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c71f6-132">System.String</span><span class="sxs-lookup"><span data-stu-id="c71f6-132">System.String</span></span>

### <span data-ttu-id="c71f6-133">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c71f6-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c71f6-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c71f6-134">OUTPUTS</span></span>

### <span data-ttu-id="c71f6-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c71f6-135">System.Boolean</span></span>

## <span data-ttu-id="c71f6-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c71f6-136">NOTES</span></span>

## <span data-ttu-id="c71f6-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c71f6-137">RELATED LINKS</span></span>

[<span data-ttu-id="c71f6-138">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="c71f6-138">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="c71f6-139">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="c71f6-139">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="c71f6-140">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="c71f6-140">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="c71f6-141">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="c71f6-141">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="c71f6-142">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="c71f6-142">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)
