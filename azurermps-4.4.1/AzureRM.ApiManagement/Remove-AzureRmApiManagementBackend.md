---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
ms.openlocfilehash: 03f56a17d038407b3a33c09188c9a29b6f4caf09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560591"
---
# <span data-ttu-id="e3d42-101">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e3d42-101">Remove-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="e3d42-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e3d42-102">SYNOPSIS</span></span>
<span data-ttu-id="e3d42-103">Удаляет сервер.</span><span class="sxs-lookup"><span data-stu-id="e3d42-103">Removes a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3d42-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e3d42-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3d42-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3d42-105">DESCRIPTION</span></span>
<span data-ttu-id="e3d42-106">Удаляет серверные части, заданные идентификатором, из управления API.</span><span class="sxs-lookup"><span data-stu-id="e3d42-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="e3d42-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e3d42-107">EXAMPLES</span></span>

### <span data-ttu-id="e3d42-108">Пример 1: удаление внутреннего сервера 123</span><span class="sxs-lookup"><span data-stu-id="e3d42-108">Example 1: Remove the Backend 123</span></span>
```
Remove-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="e3d42-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e3d42-109">PARAMETERS</span></span>

### <span data-ttu-id="e3d42-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="e3d42-110">-BackendId</span></span>
<span data-ttu-id="e3d42-111">Идентификатор существующей базы данных.</span><span class="sxs-lookup"><span data-stu-id="e3d42-111">Identifier of existing backend.</span></span>
<span data-ttu-id="e3d42-112">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="e3d42-112">This parameter is required.</span></span>

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

### <span data-ttu-id="e3d42-113">-Context</span><span class="sxs-lookup"><span data-stu-id="e3d42-113">-Context</span></span>
<span data-ttu-id="e3d42-114">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="e3d42-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e3d42-115">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="e3d42-115">This parameter is required.</span></span>

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

### <span data-ttu-id="e3d42-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3d42-116">-PassThru</span></span>
<span data-ttu-id="e3d42-117">Если задано значение true, операция Case запишется успешно.</span><span class="sxs-lookup"><span data-stu-id="e3d42-117">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="e3d42-118">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="e3d42-118">This parameter is optional.</span></span>
<span data-ttu-id="e3d42-119">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="e3d42-119">Default value is false.</span></span>

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

### <span data-ttu-id="e3d42-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3d42-120">-Confirm</span></span>
<span data-ttu-id="e3d42-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e3d42-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3d42-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3d42-122">-WhatIf</span></span>
<span data-ttu-id="e3d42-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e3d42-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e3d42-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e3d42-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3d42-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3d42-125">-DefaultProfile</span></span>
<span data-ttu-id="e3d42-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e3d42-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3d42-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3d42-127">CommonParameters</span></span>
<span data-ttu-id="e3d42-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e3d42-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3d42-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3d42-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3d42-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e3d42-130">INPUTS</span></span>

## <span data-ttu-id="e3d42-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3d42-131">OUTPUTS</span></span>

### <span data-ttu-id="e3d42-132">логических</span><span class="sxs-lookup"><span data-stu-id="e3d42-132">bool</span></span>

## <span data-ttu-id="e3d42-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="e3d42-133">NOTES</span></span>

## <span data-ttu-id="e3d42-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e3d42-134">RELATED LINKS</span></span>

[<span data-ttu-id="e3d42-135">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e3d42-135">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="e3d42-136">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e3d42-136">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="e3d42-137">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="e3d42-137">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="e3d42-138">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="e3d42-138">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="e3d42-139">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e3d42-139">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)
