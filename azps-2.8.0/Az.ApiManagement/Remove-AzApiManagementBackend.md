---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
ms.openlocfilehash: 55a78bbf03ae82b0d861a89dfd6e843399580bef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727994"
---
# <span data-ttu-id="9c7f9-101">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="9c7f9-101">Remove-AzApiManagementBackend</span></span>

## <span data-ttu-id="9c7f9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9c7f9-102">SYNOPSIS</span></span>
<span data-ttu-id="9c7f9-103">Удаляет сервер.</span><span class="sxs-lookup"><span data-stu-id="9c7f9-103">Removes a Backend.</span></span>

## <span data-ttu-id="9c7f9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9c7f9-104">SYNTAX</span></span>

```
Remove-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c7f9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c7f9-105">DESCRIPTION</span></span>
<span data-ttu-id="9c7f9-106">Удаляет серверные части, заданные идентификатором, из управления API.</span><span class="sxs-lookup"><span data-stu-id="9c7f9-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="9c7f9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9c7f9-107">EXAMPLES</span></span>

### <span data-ttu-id="9c7f9-108">Пример 1: удаление внутреннего сервера 123</span><span class="sxs-lookup"><span data-stu-id="9c7f9-108">Example 1: Remove the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="9c7f9-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9c7f9-109">PARAMETERS</span></span>

### <span data-ttu-id="9c7f9-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="9c7f9-110">-BackendId</span></span>
<span data-ttu-id="9c7f9-111">Идентификатор существующей базы данных.</span><span class="sxs-lookup"><span data-stu-id="9c7f9-111">Identifier of existing backend.</span></span>
<span data-ttu-id="9c7f9-112">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="9c7f9-112">This parameter is required.</span></span>

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

### <span data-ttu-id="9c7f9-113">-Context</span><span class="sxs-lookup"><span data-stu-id="9c7f9-113">-Context</span></span>
<span data-ttu-id="9c7f9-114">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="9c7f9-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9c7f9-115">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="9c7f9-115">This parameter is required.</span></span>

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

### <span data-ttu-id="9c7f9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c7f9-116">-DefaultProfile</span></span>
<span data-ttu-id="9c7f9-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9c7f9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c7f9-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c7f9-118">-PassThru</span></span>
<span data-ttu-id="9c7f9-119">Если задано значение true, операция Case запишется успешно.</span><span class="sxs-lookup"><span data-stu-id="9c7f9-119">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="9c7f9-120">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9c7f9-120">This parameter is optional.</span></span>
<span data-ttu-id="9c7f9-121">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="9c7f9-121">Default value is false.</span></span>

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

### <span data-ttu-id="9c7f9-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9c7f9-122">-Confirm</span></span>
<span data-ttu-id="9c7f9-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9c7f9-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c7f9-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c7f9-124">-WhatIf</span></span>
<span data-ttu-id="9c7f9-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9c7f9-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9c7f9-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9c7f9-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c7f9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c7f9-127">CommonParameters</span></span>
<span data-ttu-id="9c7f9-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9c7f9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c7f9-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c7f9-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c7f9-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9c7f9-130">INPUTS</span></span>

### <span data-ttu-id="9c7f9-131">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9c7f9-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9c7f9-132">System. String</span><span class="sxs-lookup"><span data-stu-id="9c7f9-132">System.String</span></span>

### <span data-ttu-id="9c7f9-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9c7f9-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9c7f9-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c7f9-134">OUTPUTS</span></span>

### <span data-ttu-id="9c7f9-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9c7f9-135">System.Boolean</span></span>

## <span data-ttu-id="9c7f9-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="9c7f9-136">NOTES</span></span>

## <span data-ttu-id="9c7f9-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9c7f9-137">RELATED LINKS</span></span>

[<span data-ttu-id="9c7f9-138">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="9c7f9-138">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="9c7f9-139">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="9c7f9-139">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="9c7f9-140">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="9c7f9-140">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="9c7f9-141">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="9c7f9-141">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="9c7f9-142">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="9c7f9-142">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)
