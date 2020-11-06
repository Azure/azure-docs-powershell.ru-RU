---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApi.md
ms.openlocfilehash: d84efcf68885e6d2e39ae15944c5f60298044ab7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558643"
---
# <span data-ttu-id="c0b77-101">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c0b77-101">Get-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="c0b77-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c0b77-102">SYNOPSIS</span></span>
<span data-ttu-id="c0b77-103">Возвращает API.</span><span class="sxs-lookup"><span data-stu-id="c0b77-103">Gets an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0b77-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c0b77-104">SYNTAX</span></span>

### <span data-ttu-id="c0b77-105">GetAllApis (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c0b77-105">GetAllApis (Default)</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c0b77-106">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="c0b77-106">GetByApiId</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0b77-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="c0b77-107">GetByName</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0b77-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="c0b77-108">GetByProductId</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0b77-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0b77-109">DESCRIPTION</span></span>
<span data-ttu-id="c0b77-110">Командлет **Get-AzureRmApiManagementApi** получает один или несколько API для управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="c0b77-110">The **Get-AzureRmApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="c0b77-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c0b77-111">EXAMPLES</span></span>

### <span data-ttu-id="c0b77-112">Пример 1: получение всех API-интерфейсов управления</span><span class="sxs-lookup"><span data-stu-id="c0b77-112">Example 1: Get all management APIs</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="c0b77-113">Эта команда получает все API для заданного контекста.</span><span class="sxs-lookup"><span data-stu-id="c0b77-113">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="c0b77-114">Пример 2: получение API управления по ИДЕНТИФИКАТОРу</span><span class="sxs-lookup"><span data-stu-id="c0b77-114">Example 2: Get a management API by ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="c0b77-115">Эта команда возвращает API с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="c0b77-115">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="c0b77-116">Пример 3: получение API-интерфейса управления по имени</span><span class="sxs-lookup"><span data-stu-id="c0b77-116">Example 3: Get a management API by name</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="c0b77-117">Эта команда возвращает API с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="c0b77-117">This command gets the API with the specified name.</span></span>

## <span data-ttu-id="c0b77-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c0b77-118">PARAMETERS</span></span>

### <span data-ttu-id="c0b77-119">-ApiId</span><span class="sxs-lookup"><span data-stu-id="c0b77-119">-ApiId</span></span>
<span data-ttu-id="c0b77-120">Указывает идентификатор API для получения.</span><span class="sxs-lookup"><span data-stu-id="c0b77-120">Specifies the ID of the API to get.</span></span>

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

### <span data-ttu-id="c0b77-121">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="c0b77-121">-ApiRevision</span></span>
<span data-ttu-id="c0b77-122">Идентификатор редакции определенной редакции API.</span><span class="sxs-lookup"><span data-stu-id="c0b77-122">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="c0b77-123">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c0b77-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="c0b77-124">-Context</span><span class="sxs-lookup"><span data-stu-id="c0b77-124">-Context</span></span>
<span data-ttu-id="c0b77-125">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="c0b77-125">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c0b77-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0b77-126">-DefaultProfile</span></span>
<span data-ttu-id="c0b77-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c0b77-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0b77-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c0b77-128">-Name</span></span>
<span data-ttu-id="c0b77-129">Указывает имя получаемого API.</span><span class="sxs-lookup"><span data-stu-id="c0b77-129">Specifies the name of the API to get.</span></span>

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

### <span data-ttu-id="c0b77-130">-ProductId</span><span class="sxs-lookup"><span data-stu-id="c0b77-130">-ProductId</span></span>
<span data-ttu-id="c0b77-131">Указывает идентификатор продукта, для которого требуется получить API.</span><span class="sxs-lookup"><span data-stu-id="c0b77-131">Specifies the ID of the product for which to get the API.</span></span>

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

### <span data-ttu-id="c0b77-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0b77-132">CommonParameters</span></span>
<span data-ttu-id="c0b77-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c0b77-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0b77-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0b77-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0b77-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c0b77-135">INPUTS</span></span>

### <span data-ttu-id="c0b77-136">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c0b77-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c0b77-137">System. String</span><span class="sxs-lookup"><span data-stu-id="c0b77-137">System.String</span></span>

## <span data-ttu-id="c0b77-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0b77-138">OUTPUTS</span></span>

### <span data-ttu-id="c0b77-139">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c0b77-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="c0b77-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="c0b77-140">NOTES</span></span>

## <span data-ttu-id="c0b77-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c0b77-141">RELATED LINKS</span></span>

[<span data-ttu-id="c0b77-142">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c0b77-142">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="c0b77-143">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c0b77-143">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="c0b77-144">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c0b77-144">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="c0b77-145">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c0b77-145">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="c0b77-146">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c0b77-146">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


