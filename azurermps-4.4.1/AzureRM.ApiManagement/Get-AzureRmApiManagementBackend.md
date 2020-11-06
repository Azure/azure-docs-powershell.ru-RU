---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
ms.openlocfilehash: 4f54b361482bad24826d7120e53f96ce8d3b9eef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566348"
---
# <span data-ttu-id="32688-101">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="32688-101">Get-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="32688-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="32688-102">SYNOPSIS</span></span>
<span data-ttu-id="32688-103">Получение подробных сведений о внутреннем сервере.</span><span class="sxs-lookup"><span data-stu-id="32688-103">Get the details of the Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32688-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="32688-104">SYNTAX</span></span>

### <span data-ttu-id="32688-105">Получение всех незавершенных последовательностей (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="32688-105">Get all backends (Default)</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="32688-106">Идентификатор для получения внутренних данных</span><span class="sxs-lookup"><span data-stu-id="32688-106">Get by backend ID</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32688-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32688-107">DESCRIPTION</span></span>
<span data-ttu-id="32688-108">Получение подробных сведений о внутреннем сервере.</span><span class="sxs-lookup"><span data-stu-id="32688-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="32688-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="32688-109">EXAMPLES</span></span>

### <span data-ttu-id="32688-110">--------------------------Пример 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="32688-110">--------------------------  Example 1  --------------------------</span></span>
<span data-ttu-id="32688-111">@ {абзац = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="32688-111">@{paragraph=PS C:\\\>}</span></span>







```
Get-AzureRmApiManagementBackend -Context $apimContext
```

<span data-ttu-id="32688-112">Получает список всех незавершенных элементов, настроенных в службе управления API.</span><span class="sxs-lookup"><span data-stu-id="32688-112">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="32688-113">--------------------------Пример 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="32688-113">--------------------------  Example 2  --------------------------</span></span>
<span data-ttu-id="32688-114">@ {абзац = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="32688-114">@{paragraph=PS C:\\\>}</span></span>







```
Get-AzureRmApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="32688-115">Получение сведений об указанной серверной части, идентифицированной с помощью идентификатора "123"</span><span class="sxs-lookup"><span data-stu-id="32688-115">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="32688-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="32688-116">PARAMETERS</span></span>

### <span data-ttu-id="32688-117">-BackendId</span><span class="sxs-lookup"><span data-stu-id="32688-117">-BackendId</span></span>
<span data-ttu-id="32688-118">Идентификатор внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="32688-118">Identifier of a backend.</span></span>
<span data-ttu-id="32688-119">Если задано значение, это попытается найти сервер по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="32688-119">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="32688-120">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="32688-120">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by backend ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32688-121">-Context</span><span class="sxs-lookup"><span data-stu-id="32688-121">-Context</span></span>
<span data-ttu-id="32688-122">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="32688-122">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="32688-123">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="32688-123">This parameter is required.</span></span>

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

### <span data-ttu-id="32688-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32688-124">-DefaultProfile</span></span>
<span data-ttu-id="32688-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="32688-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32688-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32688-126">CommonParameters</span></span>
<span data-ttu-id="32688-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="32688-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32688-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32688-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32688-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="32688-129">INPUTS</span></span>

## <span data-ttu-id="32688-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="32688-130">OUTPUTS</span></span>

### <span data-ttu-id="32688-131">IList<Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackend></span><span class="sxs-lookup"><span data-stu-id="32688-131">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend></span></span>

### <span data-ttu-id="32688-132">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementLogger. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="32688-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger.PsApiManagementBackend</span></span>

## <span data-ttu-id="32688-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="32688-133">NOTES</span></span>

## <span data-ttu-id="32688-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32688-134">RELATED LINKS</span></span>

[<span data-ttu-id="32688-135">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="32688-135">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="32688-136">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="32688-136">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="32688-137">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="32688-137">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="32688-138">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="32688-138">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="32688-139">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="32688-139">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
