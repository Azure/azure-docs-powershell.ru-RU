---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApi.md
ms.openlocfilehash: 435e167b713934962daf0cf27fc0d844caee8dcc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559387"
---
# <span data-ttu-id="fdb18-101">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fdb18-101">Get-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="fdb18-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fdb18-102">SYNOPSIS</span></span>
<span data-ttu-id="fdb18-103">Возвращает API.</span><span class="sxs-lookup"><span data-stu-id="fdb18-103">Gets an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdb18-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fdb18-104">SYNTAX</span></span>

### <span data-ttu-id="fdb18-105">GetAllApis (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fdb18-105">GetAllApis (Default)</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fdb18-106">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="fdb18-106">GetByApiId</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdb18-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="fdb18-107">GetByName</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdb18-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="fdb18-108">GetByProductId</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdb18-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fdb18-109">DESCRIPTION</span></span>
<span data-ttu-id="fdb18-110">Командлет **Get-AzureRmApiManagementApi** получает один или несколько API для управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="fdb18-110">The **Get-AzureRmApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="fdb18-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fdb18-111">EXAMPLES</span></span>

### <span data-ttu-id="fdb18-112">Пример 1: получение всех API-интерфейсов управления</span><span class="sxs-lookup"><span data-stu-id="fdb18-112">Example 1: Get all management APIs</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="fdb18-113">Эта команда получает все API для заданного контекста.</span><span class="sxs-lookup"><span data-stu-id="fdb18-113">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="fdb18-114">Пример 2: получение API управления по ИДЕНТИФИКАТОРу</span><span class="sxs-lookup"><span data-stu-id="fdb18-114">Example 2: Get a management API by ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="fdb18-115">Эта команда возвращает API с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="fdb18-115">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="fdb18-116">Пример 3: получение API-интерфейса управления по имени</span><span class="sxs-lookup"><span data-stu-id="fdb18-116">Example 3: Get a management API by name</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="fdb18-117">Эта команда возвращает API с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="fdb18-117">This command gets the API with the specified name.</span></span>

## <span data-ttu-id="fdb18-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fdb18-118">PARAMETERS</span></span>

### <span data-ttu-id="fdb18-119">-ApiId</span><span class="sxs-lookup"><span data-stu-id="fdb18-119">-ApiId</span></span>
<span data-ttu-id="fdb18-120">Указывает идентификатор API для получения.</span><span class="sxs-lookup"><span data-stu-id="fdb18-120">Specifies the ID of the API to get.</span></span>

```yaml
Type: String
Parameter Sets: GetByApiId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdb18-121">-Context</span><span class="sxs-lookup"><span data-stu-id="fdb18-121">-Context</span></span>
<span data-ttu-id="fdb18-122">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="fdb18-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="fdb18-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdb18-123">-DefaultProfile</span></span>
<span data-ttu-id="fdb18-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fdb18-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="fdb18-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fdb18-125">-Name</span></span>
<span data-ttu-id="fdb18-126">Указывает имя получаемого API.</span><span class="sxs-lookup"><span data-stu-id="fdb18-126">Specifies the name of the API to get.</span></span>

```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdb18-127">-ProductId</span><span class="sxs-lookup"><span data-stu-id="fdb18-127">-ProductId</span></span>
<span data-ttu-id="fdb18-128">Указывает идентификатор продукта, для которого требуется получить API.</span><span class="sxs-lookup"><span data-stu-id="fdb18-128">Specifies the ID of the product for which to get the API.</span></span>

```yaml
Type: String
Parameter Sets: GetByProductId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdb18-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdb18-129">CommonParameters</span></span>
<span data-ttu-id="fdb18-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fdb18-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdb18-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdb18-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdb18-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fdb18-132">INPUTS</span></span>

### <span data-ttu-id="fdb18-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="fdb18-133">None</span></span>
<span data-ttu-id="fdb18-134">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="fdb18-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fdb18-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fdb18-135">OUTPUTS</span></span>

### <span data-ttu-id="fdb18-136">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fdb18-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="fdb18-137">Сведения об API в заданной службе ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fdb18-137">The details of the Api in a given ApiManagement service</span></span>

### <span data-ttu-id="fdb18-138">IList<Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi></span><span class="sxs-lookup"><span data-stu-id="fdb18-138">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi></span></span>
<span data-ttu-id="fdb18-139">Список API в заданной службе ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fdb18-139">The list of Apis in a given ApiManagement service</span></span>

## <span data-ttu-id="fdb18-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="fdb18-140">NOTES</span></span>

## <span data-ttu-id="fdb18-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fdb18-141">RELATED LINKS</span></span>

[<span data-ttu-id="fdb18-142">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fdb18-142">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="fdb18-143">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fdb18-143">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="fdb18-144">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fdb18-144">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="fdb18-145">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fdb18-145">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="fdb18-146">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fdb18-146">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


