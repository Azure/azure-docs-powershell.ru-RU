---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
ms.openlocfilehash: 4781800ea9a6f8526ddee5e06b90b73ea676bf88
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415271"
---
# <span data-ttu-id="cce2e-101">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="cce2e-101">Get-AzApiManagementBackend</span></span>

## <span data-ttu-id="cce2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cce2e-102">SYNOPSIS</span></span>
<span data-ttu-id="cce2e-103">Получите сведения о backend.</span><span class="sxs-lookup"><span data-stu-id="cce2e-103">Get the details of the Backend.</span></span>

## <span data-ttu-id="cce2e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cce2e-104">SYNTAX</span></span>

### <span data-ttu-id="cce2e-105">ContextParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cce2e-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cce2e-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cce2e-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementBackend [-BackendId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cce2e-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cce2e-107">DESCRIPTION</span></span>
<span data-ttu-id="cce2e-108">Получите сведения о backend.</span><span class="sxs-lookup"><span data-stu-id="cce2e-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="cce2e-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cce2e-109">EXAMPLES</span></span>

### <span data-ttu-id="cce2e-110">Пример 1. Получить все backends</span><span class="sxs-lookup"><span data-stu-id="cce2e-110">Example 1: Get all Backends</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext
```

<span data-ttu-id="cce2e-111">Возвращает список всех backends, настроенных в службе управления Api.</span><span class="sxs-lookup"><span data-stu-id="cce2e-111">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="cce2e-112">Пример 2. Получить "Backend", определяемую идентификатором 123</span><span class="sxs-lookup"><span data-stu-id="cce2e-112">Example 2: Get the Backend specified by the Identifier 123</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="cce2e-113">Получить сведения о указанном backend identified by the Identifier '123'</span><span class="sxs-lookup"><span data-stu-id="cce2e-113">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="cce2e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cce2e-114">PARAMETERS</span></span>

### <span data-ttu-id="cce2e-115">-BackendId</span><span class="sxs-lookup"><span data-stu-id="cce2e-115">-BackendId</span></span>
<span data-ttu-id="cce2e-116">Идентификатор backend.</span><span class="sxs-lookup"><span data-stu-id="cce2e-116">Identifier of a backend.</span></span>
<span data-ttu-id="cce2e-117">Если он указан, будет пытаться найти подытую по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="cce2e-117">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="cce2e-118">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="cce2e-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="cce2e-119">-Контекст</span><span class="sxs-lookup"><span data-stu-id="cce2e-119">-Context</span></span>
<span data-ttu-id="cce2e-120">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="cce2e-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="cce2e-121">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="cce2e-121">This parameter is required.</span></span>

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

### <span data-ttu-id="cce2e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cce2e-122">-DefaultProfile</span></span>
<span data-ttu-id="cce2e-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cce2e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cce2e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cce2e-124">-ResourceId</span></span>
<span data-ttu-id="cce2e-125">Идентификатор ресурса Arm для backend.</span><span class="sxs-lookup"><span data-stu-id="cce2e-125">Arm Resource Identifier of the backend.</span></span> <span data-ttu-id="cce2e-126">Если он указан, будет пытаться найти подытую по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="cce2e-126">If specified will try to find backend by the identifier.</span></span> <span data-ttu-id="cce2e-127">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="cce2e-127">This parameter is required.</span></span>

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

### <span data-ttu-id="cce2e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cce2e-128">CommonParameters</span></span>
<span data-ttu-id="cce2e-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cce2e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cce2e-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cce2e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cce2e-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cce2e-131">INPUTS</span></span>

### <span data-ttu-id="cce2e-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="cce2e-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="cce2e-133">System.String</span><span class="sxs-lookup"><span data-stu-id="cce2e-133">System.String</span></span>

## <span data-ttu-id="cce2e-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cce2e-134">OUTPUTS</span></span>

### <span data-ttu-id="cce2e-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="cce2e-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="cce2e-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cce2e-136">NOTES</span></span>

## <span data-ttu-id="cce2e-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cce2e-137">RELATED LINKS</span></span>

[<span data-ttu-id="cce2e-138">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="cce2e-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="cce2e-139">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="cce2e-139">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="cce2e-140">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="cce2e-140">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="cce2e-141">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="cce2e-141">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="cce2e-142">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="cce2e-142">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
