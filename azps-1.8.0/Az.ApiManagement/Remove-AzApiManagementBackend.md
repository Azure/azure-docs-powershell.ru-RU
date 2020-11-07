---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
ms.openlocfilehash: 3a725bf8dedec948277fac69be029375c3ab91a6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731668"
---
# <span data-ttu-id="e8cd6-101">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e8cd6-101">Remove-AzApiManagementBackend</span></span>

## <span data-ttu-id="e8cd6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e8cd6-102">SYNOPSIS</span></span>
<span data-ttu-id="e8cd6-103">Удаляет сервер.</span><span class="sxs-lookup"><span data-stu-id="e8cd6-103">Removes a Backend.</span></span>

## <span data-ttu-id="e8cd6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e8cd6-104">SYNTAX</span></span>

```
Remove-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8cd6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8cd6-105">DESCRIPTION</span></span>
<span data-ttu-id="e8cd6-106">Удаляет серверные части, заданные идентификатором, из управления API.</span><span class="sxs-lookup"><span data-stu-id="e8cd6-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="e8cd6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e8cd6-107">EXAMPLES</span></span>

### <span data-ttu-id="e8cd6-108">Пример 1: удаление внутреннего сервера 123</span><span class="sxs-lookup"><span data-stu-id="e8cd6-108">Example 1: Remove the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="e8cd6-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e8cd6-109">PARAMETERS</span></span>

### <span data-ttu-id="e8cd6-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="e8cd6-110">-BackendId</span></span>
<span data-ttu-id="e8cd6-111">Идентификатор существующей базы данных.</span><span class="sxs-lookup"><span data-stu-id="e8cd6-111">Identifier of existing backend.</span></span>
<span data-ttu-id="e8cd6-112">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="e8cd6-112">This parameter is required.</span></span>

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

### <span data-ttu-id="e8cd6-113">-Context</span><span class="sxs-lookup"><span data-stu-id="e8cd6-113">-Context</span></span>
<span data-ttu-id="e8cd6-114">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="e8cd6-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e8cd6-115">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="e8cd6-115">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8cd6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8cd6-116">-DefaultProfile</span></span>
<span data-ttu-id="e8cd6-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e8cd6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8cd6-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8cd6-118">-PassThru</span></span>
<span data-ttu-id="e8cd6-119">Если задано значение true, операция Case запишется успешно.</span><span class="sxs-lookup"><span data-stu-id="e8cd6-119">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="e8cd6-120">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="e8cd6-120">This parameter is optional.</span></span>
<span data-ttu-id="e8cd6-121">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="e8cd6-121">Default value is false.</span></span>

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

### <span data-ttu-id="e8cd6-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e8cd6-122">-Confirm</span></span>
<span data-ttu-id="e8cd6-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e8cd6-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8cd6-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8cd6-124">-WhatIf</span></span>
<span data-ttu-id="e8cd6-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e8cd6-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e8cd6-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e8cd6-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8cd6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8cd6-127">CommonParameters</span></span>
<span data-ttu-id="e8cd6-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e8cd6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8cd6-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8cd6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8cd6-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e8cd6-130">INPUTS</span></span>

### <span data-ttu-id="e8cd6-131">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e8cd6-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e8cd6-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e8cd6-132">System.String</span></span>

### <span data-ttu-id="e8cd6-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e8cd6-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e8cd6-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8cd6-134">OUTPUTS</span></span>

### <span data-ttu-id="e8cd6-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e8cd6-135">System.Boolean</span></span>

## <span data-ttu-id="e8cd6-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="e8cd6-136">NOTES</span></span>

## <span data-ttu-id="e8cd6-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e8cd6-137">RELATED LINKS</span></span>

[<span data-ttu-id="e8cd6-138">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e8cd6-138">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="e8cd6-139">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e8cd6-139">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="e8cd6-140">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="e8cd6-140">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="e8cd6-141">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="e8cd6-141">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="e8cd6-142">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e8cd6-142">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)
