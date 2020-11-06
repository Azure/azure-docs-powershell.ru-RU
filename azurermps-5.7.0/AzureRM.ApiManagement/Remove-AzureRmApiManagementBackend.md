---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
ms.openlocfilehash: 347a05c5e197a93458a64c4079ce1fd430e631f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565036"
---
# <span data-ttu-id="dadc3-101">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="dadc3-101">Remove-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="dadc3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dadc3-102">SYNOPSIS</span></span>
<span data-ttu-id="dadc3-103">Удаляет сервер.</span><span class="sxs-lookup"><span data-stu-id="dadc3-103">Removes a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dadc3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dadc3-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dadc3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dadc3-105">DESCRIPTION</span></span>
<span data-ttu-id="dadc3-106">Удаляет серверные части, заданные идентификатором, из управления API.</span><span class="sxs-lookup"><span data-stu-id="dadc3-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="dadc3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dadc3-107">EXAMPLES</span></span>

### <span data-ttu-id="dadc3-108">Пример 1: удаление внутреннего сервера 123</span><span class="sxs-lookup"><span data-stu-id="dadc3-108">Example 1: Remove the Backend 123</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="dadc3-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dadc3-109">PARAMETERS</span></span>

### <span data-ttu-id="dadc3-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="dadc3-110">-BackendId</span></span>
<span data-ttu-id="dadc3-111">Идентификатор существующей базы данных.</span><span class="sxs-lookup"><span data-stu-id="dadc3-111">Identifier of existing backend.</span></span>
<span data-ttu-id="dadc3-112">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="dadc3-112">This parameter is required.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dadc3-113">-Context</span><span class="sxs-lookup"><span data-stu-id="dadc3-113">-Context</span></span>
<span data-ttu-id="dadc3-114">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="dadc3-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="dadc3-115">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="dadc3-115">This parameter is required.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dadc3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dadc3-116">-DefaultProfile</span></span>
<span data-ttu-id="dadc3-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dadc3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dadc3-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dadc3-118">-PassThru</span></span>
<span data-ttu-id="dadc3-119">Если задано значение true, операция Case запишется успешно.</span><span class="sxs-lookup"><span data-stu-id="dadc3-119">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="dadc3-120">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="dadc3-120">This parameter is optional.</span></span>
<span data-ttu-id="dadc3-121">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="dadc3-121">Default value is false.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dadc3-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dadc3-122">-Confirm</span></span>
<span data-ttu-id="dadc3-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dadc3-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dadc3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dadc3-124">-WhatIf</span></span>
<span data-ttu-id="dadc3-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dadc3-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dadc3-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dadc3-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dadc3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dadc3-127">CommonParameters</span></span>
<span data-ttu-id="dadc3-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dadc3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dadc3-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dadc3-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dadc3-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dadc3-130">INPUTS</span></span>

### <span data-ttu-id="dadc3-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="dadc3-131">None</span></span>
<span data-ttu-id="dadc3-132">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="dadc3-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dadc3-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dadc3-133">OUTPUTS</span></span>

### <span data-ttu-id="dadc3-134">логических</span><span class="sxs-lookup"><span data-stu-id="dadc3-134">bool</span></span>

## <span data-ttu-id="dadc3-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="dadc3-135">NOTES</span></span>

## <span data-ttu-id="dadc3-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dadc3-136">RELATED LINKS</span></span>

[<span data-ttu-id="dadc3-137">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="dadc3-137">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="dadc3-138">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="dadc3-138">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="dadc3-139">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="dadc3-139">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="dadc3-140">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="dadc3-140">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="dadc3-141">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="dadc3-141">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)
