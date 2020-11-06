---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
ms.openlocfilehash: ef00a5140dc25065c05494211721c5773a9b5243
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556948"
---
# <span data-ttu-id="d7c43-101">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d7c43-101">Remove-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="d7c43-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d7c43-102">SYNOPSIS</span></span>
<span data-ttu-id="d7c43-103">Удаляет сервер.</span><span class="sxs-lookup"><span data-stu-id="d7c43-103">Removes a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7c43-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d7c43-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7c43-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7c43-105">DESCRIPTION</span></span>
<span data-ttu-id="d7c43-106">Удаляет серверные части, заданные идентификатором, из управления API.</span><span class="sxs-lookup"><span data-stu-id="d7c43-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="d7c43-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d7c43-107">EXAMPLES</span></span>

### <span data-ttu-id="d7c43-108">Пример 1: удаление внутреннего сервера 123</span><span class="sxs-lookup"><span data-stu-id="d7c43-108">Example 1: Remove the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="d7c43-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d7c43-109">PARAMETERS</span></span>

### <span data-ttu-id="d7c43-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="d7c43-110">-BackendId</span></span>
<span data-ttu-id="d7c43-111">Идентификатор существующей базы данных.</span><span class="sxs-lookup"><span data-stu-id="d7c43-111">Identifier of existing backend.</span></span>
<span data-ttu-id="d7c43-112">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="d7c43-112">This parameter is required.</span></span>

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

### <span data-ttu-id="d7c43-113">-Context</span><span class="sxs-lookup"><span data-stu-id="d7c43-113">-Context</span></span>
<span data-ttu-id="d7c43-114">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d7c43-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d7c43-115">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="d7c43-115">This parameter is required.</span></span>

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

### <span data-ttu-id="d7c43-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7c43-116">-DefaultProfile</span></span>
<span data-ttu-id="d7c43-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d7c43-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7c43-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7c43-118">-PassThru</span></span>
<span data-ttu-id="d7c43-119">Если задано значение true, операция Case запишется успешно.</span><span class="sxs-lookup"><span data-stu-id="d7c43-119">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="d7c43-120">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="d7c43-120">This parameter is optional.</span></span>
<span data-ttu-id="d7c43-121">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="d7c43-121">Default value is false.</span></span>

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

### <span data-ttu-id="d7c43-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7c43-122">-Confirm</span></span>
<span data-ttu-id="d7c43-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d7c43-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7c43-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7c43-124">-WhatIf</span></span>
<span data-ttu-id="d7c43-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d7c43-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d7c43-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d7c43-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7c43-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7c43-127">CommonParameters</span></span>
<span data-ttu-id="d7c43-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d7c43-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7c43-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7c43-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7c43-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d7c43-130">INPUTS</span></span>

### <span data-ttu-id="d7c43-131">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d7c43-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d7c43-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d7c43-132">System.String</span></span>

### <span data-ttu-id="d7c43-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d7c43-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d7c43-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7c43-134">OUTPUTS</span></span>

### <span data-ttu-id="d7c43-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d7c43-135">System.Boolean</span></span>

## <span data-ttu-id="d7c43-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="d7c43-136">NOTES</span></span>

## <span data-ttu-id="d7c43-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d7c43-137">RELATED LINKS</span></span>

[<span data-ttu-id="d7c43-138">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d7c43-138">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="d7c43-139">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d7c43-139">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="d7c43-140">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="d7c43-140">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="d7c43-141">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="d7c43-141">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="d7c43-142">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d7c43-142">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)
