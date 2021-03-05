---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
ms.openlocfilehash: 5e1cbec98e2b501a71f022766f7248c3209d590f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991749"
---
# <span data-ttu-id="3750e-101">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="3750e-101">Get-AzApiManagementApi</span></span>

## <span data-ttu-id="3750e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3750e-102">SYNOPSIS</span></span>
<span data-ttu-id="3750e-103">Получает API.</span><span class="sxs-lookup"><span data-stu-id="3750e-103">Gets an API.</span></span>

## <span data-ttu-id="3750e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3750e-104">SYNTAX</span></span>

### <span data-ttu-id="3750e-105">GetAllApis (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3750e-105">GetAllApis (Default)</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3750e-106">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="3750e-106">GetByApiId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3750e-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="3750e-107">GetByName</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3750e-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="3750e-108">GetByProductId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3750e-109">GetByGatewayId</span><span class="sxs-lookup"><span data-stu-id="3750e-109">GetByGatewayId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3750e-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3750e-110">DESCRIPTION</span></span>
<span data-ttu-id="3750e-111">Для получения одного или более API-API Azure API возвращается один или несколько API-API **Get-AzApiManagementApi.**</span><span class="sxs-lookup"><span data-stu-id="3750e-111">The **Get-AzApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="3750e-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3750e-112">EXAMPLES</span></span>

### <span data-ttu-id="3750e-113">Пример 1. Получите все API управления</span><span class="sxs-lookup"><span data-stu-id="3750e-113">Example 1: Get all management APIs</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="3750e-114">Эта команда получает все API для заданного контекста.</span><span class="sxs-lookup"><span data-stu-id="3750e-114">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="3750e-115">Пример 2. Получите API управления по ИД</span><span class="sxs-lookup"><span data-stu-id="3750e-115">Example 2: Get a management API by ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="3750e-116">Эта команда получает API с указанным ИД.</span><span class="sxs-lookup"><span data-stu-id="3750e-116">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="3750e-117">Пример 3. Получите API управления по имени</span><span class="sxs-lookup"><span data-stu-id="3750e-117">Example 3: Get a management API by name</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="3750e-118">Эта команда получает API с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="3750e-118">This command gets the API with the specified name.</span></span>

### <span data-ttu-id="3750e-119">Пример 4. Получите API управления по GatewayId</span><span class="sxs-lookup"><span data-stu-id="3750e-119">Example 4: Get a management API by GatewayId</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -GatewayId "g01"
```

<span data-ttu-id="3750e-120">Эта команда получает API для указанного ИД Шлюза.</span><span class="sxs-lookup"><span data-stu-id="3750e-120">This command gets the API for the specified GatewayId.</span></span>

## <span data-ttu-id="3750e-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3750e-121">PARAMETERS</span></span>

### <span data-ttu-id="3750e-122">-ApiId</span><span class="sxs-lookup"><span data-stu-id="3750e-122">-ApiId</span></span>
<span data-ttu-id="3750e-123">Определяет ИД API, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="3750e-123">Specifies the ID of the API to get.</span></span>

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

### <span data-ttu-id="3750e-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="3750e-124">-ApiRevision</span></span>
<span data-ttu-id="3750e-125">Идентификатор редакции определенного изменения API.</span><span class="sxs-lookup"><span data-stu-id="3750e-125">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="3750e-126">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="3750e-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="3750e-127">-Контекст</span><span class="sxs-lookup"><span data-stu-id="3750e-127">-Context</span></span>
<span data-ttu-id="3750e-128">Указывает объект **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="3750e-128">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3750e-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3750e-129">-DefaultProfile</span></span>
<span data-ttu-id="3750e-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3750e-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3750e-131">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="3750e-131">-GatewayId</span></span>
<span data-ttu-id="3750e-132">Если задан этот пункт, будет пытаться получить все API шлюза.</span><span class="sxs-lookup"><span data-stu-id="3750e-132">If specified will try to get all Gateway APIs.</span></span>

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

### <span data-ttu-id="3750e-133">-Name</span><span class="sxs-lookup"><span data-stu-id="3750e-133">-Name</span></span>
<span data-ttu-id="3750e-134">Указывает имя API, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="3750e-134">Specifies the name of the API to get.</span></span>

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

### <span data-ttu-id="3750e-135">-ProductId</span><span class="sxs-lookup"><span data-stu-id="3750e-135">-ProductId</span></span>
<span data-ttu-id="3750e-136">Определяет ИД продукта, для которого требуется получить API.</span><span class="sxs-lookup"><span data-stu-id="3750e-136">Specifies the ID of the product for which to get the API.</span></span>

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

### <span data-ttu-id="3750e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3750e-137">CommonParameters</span></span>
<span data-ttu-id="3750e-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3750e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3750e-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3750e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3750e-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3750e-140">INPUTS</span></span>

### <span data-ttu-id="3750e-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3750e-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3750e-142">System.String</span><span class="sxs-lookup"><span data-stu-id="3750e-142">System.String</span></span>

## <span data-ttu-id="3750e-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3750e-143">OUTPUTS</span></span>

### <span data-ttu-id="3750e-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="3750e-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="3750e-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3750e-145">NOTES</span></span>

## <span data-ttu-id="3750e-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3750e-146">RELATED LINKS</span></span>

[<span data-ttu-id="3750e-147">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="3750e-147">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="3750e-148">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="3750e-148">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="3750e-149">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="3750e-149">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="3750e-150">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="3750e-150">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="3750e-151">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="3750e-151">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


