---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
ms.openlocfilehash: a87c75058e3ebfb1ae7d14e729fdc9280cdccb9c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720171"
---
# <span data-ttu-id="01631-101">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="01631-101">Get-AzApiManagementApi</span></span>

## <span data-ttu-id="01631-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="01631-102">SYNOPSIS</span></span>
<span data-ttu-id="01631-103">Возвращает API.</span><span class="sxs-lookup"><span data-stu-id="01631-103">Gets an API.</span></span>

## <span data-ttu-id="01631-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="01631-104">SYNTAX</span></span>

### <span data-ttu-id="01631-105">GetAllApis (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="01631-105">GetAllApis (Default)</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="01631-106">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="01631-106">GetByApiId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01631-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="01631-107">GetByName</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01631-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="01631-108">GetByProductId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01631-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="01631-109">DESCRIPTION</span></span>
<span data-ttu-id="01631-110">Командлет **Get-AzApiManagementApi** получает один или несколько API для управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="01631-110">The **Get-AzApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="01631-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="01631-111">EXAMPLES</span></span>

### <span data-ttu-id="01631-112">Пример 1: получение всех API-интерфейсов управления</span><span class="sxs-lookup"><span data-stu-id="01631-112">Example 1: Get all management APIs</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="01631-113">Эта команда получает все API для заданного контекста.</span><span class="sxs-lookup"><span data-stu-id="01631-113">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="01631-114">Пример 2: получение API управления по ИДЕНТИФИКАТОРу</span><span class="sxs-lookup"><span data-stu-id="01631-114">Example 2: Get a management API by ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="01631-115">Эта команда возвращает API с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="01631-115">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="01631-116">Пример 3: получение API-интерфейса управления по имени</span><span class="sxs-lookup"><span data-stu-id="01631-116">Example 3: Get a management API by name</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="01631-117">Эта команда возвращает API с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="01631-117">This command gets the API with the specified name.</span></span>

## <span data-ttu-id="01631-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="01631-118">PARAMETERS</span></span>

### <span data-ttu-id="01631-119">-ApiId</span><span class="sxs-lookup"><span data-stu-id="01631-119">-ApiId</span></span>
<span data-ttu-id="01631-120">Указывает идентификатор API для получения.</span><span class="sxs-lookup"><span data-stu-id="01631-120">Specifies the ID of the API to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01631-121">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="01631-121">-ApiRevision</span></span>
<span data-ttu-id="01631-122">Идентификатор редакции определенной редакции API.</span><span class="sxs-lookup"><span data-stu-id="01631-122">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="01631-123">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="01631-123">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByApiId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01631-124">-Context</span><span class="sxs-lookup"><span data-stu-id="01631-124">-Context</span></span>
<span data-ttu-id="01631-125">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="01631-125">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="01631-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01631-126">-DefaultProfile</span></span>
<span data-ttu-id="01631-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="01631-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01631-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="01631-128">-Name</span></span>
<span data-ttu-id="01631-129">Указывает имя получаемого API.</span><span class="sxs-lookup"><span data-stu-id="01631-129">Specifies the name of the API to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01631-130">-ProductId</span><span class="sxs-lookup"><span data-stu-id="01631-130">-ProductId</span></span>
<span data-ttu-id="01631-131">Указывает идентификатор продукта, для которого требуется получить API.</span><span class="sxs-lookup"><span data-stu-id="01631-131">Specifies the ID of the product for which to get the API.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01631-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01631-132">CommonParameters</span></span>
<span data-ttu-id="01631-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="01631-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01631-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01631-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01631-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="01631-135">INPUTS</span></span>

### <span data-ttu-id="01631-136">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="01631-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="01631-137">System. String</span><span class="sxs-lookup"><span data-stu-id="01631-137">System.String</span></span>

## <span data-ttu-id="01631-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="01631-138">OUTPUTS</span></span>

### <span data-ttu-id="01631-139">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="01631-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="01631-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="01631-140">NOTES</span></span>

## <span data-ttu-id="01631-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="01631-141">RELATED LINKS</span></span>

[<span data-ttu-id="01631-142">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="01631-142">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="01631-143">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="01631-143">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="01631-144">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="01631-144">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="01631-145">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="01631-145">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="01631-146">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="01631-146">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


