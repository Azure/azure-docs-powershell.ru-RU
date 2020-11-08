---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
ms.openlocfilehash: 8b6f27191ee92240a8dc9e5e8289fda72db856ab
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244208"
---
# <span data-ttu-id="15ddc-101">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="15ddc-101">Get-AzApiManagementApi</span></span>

## <span data-ttu-id="15ddc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="15ddc-102">SYNOPSIS</span></span>
<span data-ttu-id="15ddc-103">Возвращает API.</span><span class="sxs-lookup"><span data-stu-id="15ddc-103">Gets an API.</span></span>

## <span data-ttu-id="15ddc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="15ddc-104">SYNTAX</span></span>

### <span data-ttu-id="15ddc-105">GetAllApis (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="15ddc-105">GetAllApis (Default)</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="15ddc-106">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="15ddc-106">GetByApiId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15ddc-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="15ddc-107">GetByName</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15ddc-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="15ddc-108">GetByProductId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15ddc-109">GetByGatewayId</span><span class="sxs-lookup"><span data-stu-id="15ddc-109">GetByGatewayId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15ddc-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="15ddc-110">DESCRIPTION</span></span>
<span data-ttu-id="15ddc-111">Командлет **Get-AzApiManagementApi** получает один или несколько API для управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="15ddc-111">The **Get-AzApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="15ddc-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="15ddc-112">EXAMPLES</span></span>

### <span data-ttu-id="15ddc-113">Пример 1: получение всех API-интерфейсов управления</span><span class="sxs-lookup"><span data-stu-id="15ddc-113">Example 1: Get all management APIs</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="15ddc-114">Эта команда получает все API для заданного контекста.</span><span class="sxs-lookup"><span data-stu-id="15ddc-114">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="15ddc-115">Пример 2: получение API управления по ИДЕНТИФИКАТОРу</span><span class="sxs-lookup"><span data-stu-id="15ddc-115">Example 2: Get a management API by ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="15ddc-116">Эта команда возвращает API с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="15ddc-116">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="15ddc-117">Пример 3: получение API-интерфейса управления по имени</span><span class="sxs-lookup"><span data-stu-id="15ddc-117">Example 3: Get a management API by name</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="15ddc-118">Эта команда возвращает API с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="15ddc-118">This command gets the API with the specified name.</span></span>

### <span data-ttu-id="15ddc-119">Пример 4: получение API управления с помощью GatewayId</span><span class="sxs-lookup"><span data-stu-id="15ddc-119">Example 4: Get a management API by GatewayId</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -GatewayId "g01"
```

<span data-ttu-id="15ddc-120">Эта команда возвращает API для указанного GatewayId.</span><span class="sxs-lookup"><span data-stu-id="15ddc-120">This command gets the API for the specified GatewayId.</span></span>

## <span data-ttu-id="15ddc-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="15ddc-121">PARAMETERS</span></span>

### <span data-ttu-id="15ddc-122">-ApiId</span><span class="sxs-lookup"><span data-stu-id="15ddc-122">-ApiId</span></span>
<span data-ttu-id="15ddc-123">Указывает идентификатор API для получения.</span><span class="sxs-lookup"><span data-stu-id="15ddc-123">Specifies the ID of the API to get.</span></span>

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

### <span data-ttu-id="15ddc-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="15ddc-124">-ApiRevision</span></span>
<span data-ttu-id="15ddc-125">Идентификатор редакции определенной редакции API.</span><span class="sxs-lookup"><span data-stu-id="15ddc-125">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="15ddc-126">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="15ddc-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="15ddc-127">-Context</span><span class="sxs-lookup"><span data-stu-id="15ddc-127">-Context</span></span>
<span data-ttu-id="15ddc-128">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="15ddc-128">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="15ddc-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15ddc-129">-DefaultProfile</span></span>
<span data-ttu-id="15ddc-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="15ddc-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15ddc-131">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="15ddc-131">-GatewayId</span></span>
<span data-ttu-id="15ddc-132">Если указано, попытается получить все API шлюза.</span><span class="sxs-lookup"><span data-stu-id="15ddc-132">If specified will try to get all Gateway APIs.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByGatewayId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15ddc-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="15ddc-133">-Name</span></span>
<span data-ttu-id="15ddc-134">Указывает имя получаемого API.</span><span class="sxs-lookup"><span data-stu-id="15ddc-134">Specifies the name of the API to get.</span></span>

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

### <span data-ttu-id="15ddc-135">-ProductId</span><span class="sxs-lookup"><span data-stu-id="15ddc-135">-ProductId</span></span>
<span data-ttu-id="15ddc-136">Указывает идентификатор продукта, для которого требуется получить API.</span><span class="sxs-lookup"><span data-stu-id="15ddc-136">Specifies the ID of the product for which to get the API.</span></span>

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

### <span data-ttu-id="15ddc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15ddc-137">CommonParameters</span></span>
<span data-ttu-id="15ddc-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="15ddc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15ddc-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15ddc-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15ddc-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="15ddc-140">INPUTS</span></span>

### <span data-ttu-id="15ddc-141">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="15ddc-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="15ddc-142">System. String</span><span class="sxs-lookup"><span data-stu-id="15ddc-142">System.String</span></span>

## <span data-ttu-id="15ddc-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="15ddc-143">OUTPUTS</span></span>

### <span data-ttu-id="15ddc-144">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="15ddc-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="15ddc-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="15ddc-145">NOTES</span></span>

## <span data-ttu-id="15ddc-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="15ddc-146">RELATED LINKS</span></span>

[<span data-ttu-id="15ddc-147">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="15ddc-147">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="15ddc-148">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="15ddc-148">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="15ddc-149">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="15ddc-149">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="15ddc-150">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="15ddc-150">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="15ddc-151">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="15ddc-151">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


