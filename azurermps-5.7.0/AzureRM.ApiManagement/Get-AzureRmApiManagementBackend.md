---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
ms.openlocfilehash: 0074ed7ec0d3aa88f813d138be71083195e6b10a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559384"
---
# <span data-ttu-id="36566-101">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="36566-101">Get-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="36566-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="36566-102">SYNOPSIS</span></span>
<span data-ttu-id="36566-103">Получение подробных сведений о внутреннем сервере.</span><span class="sxs-lookup"><span data-stu-id="36566-103">Get the details of the Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36566-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="36566-104">SYNTAX</span></span>

### <span data-ttu-id="36566-105">GetAllBackends (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="36566-105">GetAllBackends (Default)</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="36566-106">GetByBackendId</span><span class="sxs-lookup"><span data-stu-id="36566-106">GetByBackendId</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36566-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="36566-107">DESCRIPTION</span></span>
<span data-ttu-id="36566-108">Получение подробных сведений о внутреннем сервере.</span><span class="sxs-lookup"><span data-stu-id="36566-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="36566-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="36566-109">EXAMPLES</span></span>

### <span data-ttu-id="36566-110">Пример 1: получение всех незавершенных элементов</span><span class="sxs-lookup"><span data-stu-id="36566-110">Example 1: Get all Backends</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementBackend -Context $apimContext
```

<span data-ttu-id="36566-111">Получает список всех незавершенных элементов, настроенных в службе управления API.</span><span class="sxs-lookup"><span data-stu-id="36566-111">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="36566-112">Пример 2: получение серверной части, указанной идентификатором 123</span><span class="sxs-lookup"><span data-stu-id="36566-112">Example 2: Get the Backend specified by the Identifier 123</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="36566-113">Получение сведений об указанной серверной части, идентифицированной с помощью идентификатора "123"</span><span class="sxs-lookup"><span data-stu-id="36566-113">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="36566-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="36566-114">PARAMETERS</span></span>

### <span data-ttu-id="36566-115">-BackendId</span><span class="sxs-lookup"><span data-stu-id="36566-115">-BackendId</span></span>
<span data-ttu-id="36566-116">Идентификатор внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="36566-116">Identifier of a backend.</span></span>
<span data-ttu-id="36566-117">Если задано значение, это попытается найти сервер по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="36566-117">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="36566-118">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="36566-118">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByBackendId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36566-119">-Context</span><span class="sxs-lookup"><span data-stu-id="36566-119">-Context</span></span>
<span data-ttu-id="36566-120">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="36566-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="36566-121">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="36566-121">This parameter is required.</span></span>

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

### <span data-ttu-id="36566-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36566-122">-DefaultProfile</span></span>
<span data-ttu-id="36566-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="36566-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="36566-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36566-124">CommonParameters</span></span>
<span data-ttu-id="36566-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="36566-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36566-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36566-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36566-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="36566-127">INPUTS</span></span>

### <span data-ttu-id="36566-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="36566-128">None</span></span>
<span data-ttu-id="36566-129">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="36566-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="36566-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="36566-130">OUTPUTS</span></span>

### <span data-ttu-id="36566-131">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="36566-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>
<span data-ttu-id="36566-132">Сведения о серверной части, настроенной в службе управления API.</span><span class="sxs-lookup"><span data-stu-id="36566-132">The details of the Backend configured in API Management service.</span></span>

### <span data-ttu-id="36566-133">IList<Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackend></span><span class="sxs-lookup"><span data-stu-id="36566-133">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend></span></span>
<span data-ttu-id="36566-134">Список внутренних баз данных, настроенных в службе управления API.</span><span class="sxs-lookup"><span data-stu-id="36566-134">The list of Backend configured in API Management service.</span></span>

## <span data-ttu-id="36566-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="36566-135">NOTES</span></span>

## <span data-ttu-id="36566-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="36566-136">RELATED LINKS</span></span>

[<span data-ttu-id="36566-137">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="36566-137">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="36566-138">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="36566-138">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="36566-139">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="36566-139">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="36566-140">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="36566-140">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="36566-141">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="36566-141">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
