---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
ms.openlocfilehash: 4781800ea9a6f8526ddee5e06b90b73ea676bf88
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079259"
---
# <span data-ttu-id="20423-101">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="20423-101">Get-AzApiManagementBackend</span></span>

## <span data-ttu-id="20423-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="20423-102">SYNOPSIS</span></span>
<span data-ttu-id="20423-103">Получение подробных сведений о внутреннем сервере.</span><span class="sxs-lookup"><span data-stu-id="20423-103">Get the details of the Backend.</span></span>

## <span data-ttu-id="20423-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="20423-104">SYNTAX</span></span>

### <span data-ttu-id="20423-105">ContextParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="20423-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20423-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="20423-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementBackend [-BackendId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20423-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="20423-107">DESCRIPTION</span></span>
<span data-ttu-id="20423-108">Получение подробных сведений о внутреннем сервере.</span><span class="sxs-lookup"><span data-stu-id="20423-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="20423-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="20423-109">EXAMPLES</span></span>

### <span data-ttu-id="20423-110">Пример 1: получение всех незавершенных элементов</span><span class="sxs-lookup"><span data-stu-id="20423-110">Example 1: Get all Backends</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext
```

<span data-ttu-id="20423-111">Получает список всех незавершенных элементов, настроенных в службе управления API.</span><span class="sxs-lookup"><span data-stu-id="20423-111">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="20423-112">Пример 2: получение серверной части, указанной идентификатором 123</span><span class="sxs-lookup"><span data-stu-id="20423-112">Example 2: Get the Backend specified by the Identifier 123</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="20423-113">Получение сведений об указанной серверной части, идентифицированной с помощью идентификатора "123"</span><span class="sxs-lookup"><span data-stu-id="20423-113">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="20423-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="20423-114">PARAMETERS</span></span>

### <span data-ttu-id="20423-115">-BackendId</span><span class="sxs-lookup"><span data-stu-id="20423-115">-BackendId</span></span>
<span data-ttu-id="20423-116">Идентификатор внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="20423-116">Identifier of a backend.</span></span>
<span data-ttu-id="20423-117">Если задано значение, это попытается найти сервер по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="20423-117">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="20423-118">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="20423-118">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20423-119">-Context</span><span class="sxs-lookup"><span data-stu-id="20423-119">-Context</span></span>
<span data-ttu-id="20423-120">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="20423-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="20423-121">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="20423-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20423-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20423-122">-DefaultProfile</span></span>
<span data-ttu-id="20423-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="20423-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20423-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="20423-124">-ResourceId</span></span>
<span data-ttu-id="20423-125">Идентификатор ресурса ARM для внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="20423-125">Arm Resource Identifier of the backend.</span></span> <span data-ttu-id="20423-126">Если задано значение, это попытается найти сервер по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="20423-126">If specified will try to find backend by the identifier.</span></span> <span data-ttu-id="20423-127">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="20423-127">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20423-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20423-128">CommonParameters</span></span>
<span data-ttu-id="20423-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="20423-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20423-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20423-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20423-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="20423-131">INPUTS</span></span>

### <span data-ttu-id="20423-132">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="20423-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="20423-133">System. String</span><span class="sxs-lookup"><span data-stu-id="20423-133">System.String</span></span>

## <span data-ttu-id="20423-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="20423-134">OUTPUTS</span></span>

### <span data-ttu-id="20423-135">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="20423-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="20423-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="20423-136">NOTES</span></span>

## <span data-ttu-id="20423-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="20423-137">RELATED LINKS</span></span>

[<span data-ttu-id="20423-138">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="20423-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="20423-139">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="20423-139">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="20423-140">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="20423-140">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="20423-141">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="20423-141">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="20423-142">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="20423-142">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
