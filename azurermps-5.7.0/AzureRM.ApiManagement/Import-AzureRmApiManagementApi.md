---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 48C143BE-3BF6-43E3-99B0-1A1D12A0A3F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/import-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementApi.md
ms.openlocfilehash: 5e00f3718b093f3112839ebb331fc96984a03038
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734497"
---
# <span data-ttu-id="21371-101">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="21371-101">Import-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="21371-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="21371-102">SYNOPSIS</span></span>
<span data-ttu-id="21371-103">Импортирует API из файла или URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="21371-103">Imports an API from a file or a URL.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21371-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="21371-104">SYNTAX</span></span>

### <span data-ttu-id="21371-105">ImportFromLocalFile (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="21371-105">ImportFromLocalFile (Default)</span></span>
```
Import-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationPath <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21371-106">ImportFromUrl</span><span class="sxs-lookup"><span data-stu-id="21371-106">ImportFromUrl</span></span>
```
Import-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationUrl <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21371-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="21371-107">DESCRIPTION</span></span>
<span data-ttu-id="21371-108">Командлет **Import-AzureRmApiManagementApi** импортирует API Azure API Management из файла или URL-адреса в языке описания веб-приложений (WADL), языка описания веб-служб (WSDL) или в формате Swagger.</span><span class="sxs-lookup"><span data-stu-id="21371-108">The **Import-AzureRmApiManagementApi** cmdlet imports an Azure API Management API from a file or a URL in Web Application Description Language (WADL), Web Services Description Language (WSDL), or Swagger format.</span></span>

## <span data-ttu-id="21371-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="21371-109">EXAMPLES</span></span>

### <span data-ttu-id="21371-110">Пример 1 Импорт API из файла WADL</span><span class="sxs-lookup"><span data-stu-id="21371-110">Example 1 Import an API from a WADL file</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationPath "C:\contoso\specifications\echoapi.wadl" -Path "apis"
```

<span data-ttu-id="21371-111">Эта команда импортирует API из указанного файла WADL.</span><span class="sxs-lookup"><span data-stu-id="21371-111">This command imports an API from the specified WADL file.</span></span>

### <span data-ttu-id="21371-112">Пример 2. Импорт API из файла Swagger</span><span class="sxs-lookup"><span data-stu-id="21371-112">Example 2 Import an API from a Swagger file</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Swagger" -SpecificationPath "C:\contoso\specifications\echoapi.swagger" -Path "apis"
```

<span data-ttu-id="21371-113">Эта команда импортирует API из указанного файла Swagger.</span><span class="sxs-lookup"><span data-stu-id="21371-113">This command imports an API from the specified Swagger file.</span></span>

### <span data-ttu-id="21371-114">Пример 3: импорт API-интерфейса из ссылки WADL</span><span class="sxs-lookup"><span data-stu-id="21371-114">Example 3: Import an API from a WADL link</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationUrl "http://contoso.com/specifications/wadl/echoapi" -Path "apis"
```

<span data-ttu-id="21371-115">Эта команда импортирует API из указанной ссылки WADL.</span><span class="sxs-lookup"><span data-stu-id="21371-115">This command imports an API from the specified WADL link.</span></span>

## <span data-ttu-id="21371-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="21371-116">PARAMETERS</span></span>

### <span data-ttu-id="21371-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="21371-117">-ApiId</span></span>
<span data-ttu-id="21371-118">Указывает идентификатор API для импорта.</span><span class="sxs-lookup"><span data-stu-id="21371-118">Specifies an ID for the API to import.</span></span>
<span data-ttu-id="21371-119">Если этот параметр не указан, для вас создается идентификатор.</span><span class="sxs-lookup"><span data-stu-id="21371-119">If you do not specify this parameter, an ID is generated for you.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21371-120">-ApiType</span><span class="sxs-lookup"><span data-stu-id="21371-120">-ApiType</span></span>
<span data-ttu-id="21371-121">Этот параметр является необязательным с использованием значения по умолчанию HTTP.</span><span class="sxs-lookup"><span data-stu-id="21371-121">This parameter is optional with a default value of Http.</span></span> <span data-ttu-id="21371-122">Параметр SOAP применим только при импорте WSDL и создаст API-интерфейс для протокола SOAP PassThrough.</span><span class="sxs-lookup"><span data-stu-id="21371-122">The Soap option is only applicable when importing WSDL and will create a SOAP Passthrough API.</span></span>

```yaml
Type: PsApiManagementApiType
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Soap

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21371-123">-Context</span><span class="sxs-lookup"><span data-stu-id="21371-123">-Context</span></span>
<span data-ttu-id="21371-124">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="21371-124">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="21371-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21371-125">-DefaultProfile</span></span>
<span data-ttu-id="21371-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="21371-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="21371-127">-Path</span><span class="sxs-lookup"><span data-stu-id="21371-127">-Path</span></span>
<span data-ttu-id="21371-128">Указывает путь веб-API как последнюю часть общедоступного URL-адреса API.</span><span class="sxs-lookup"><span data-stu-id="21371-128">Specifies a web API path as the last part of the API's public URL.</span></span>
<span data-ttu-id="21371-129">Этот URL-адрес используется клиентами API для отправки запросов на веб-службу.</span><span class="sxs-lookup"><span data-stu-id="21371-129">This URL is used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="21371-130">Должно содержать от 1 до 400 символов.</span><span class="sxs-lookup"><span data-stu-id="21371-130">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="21371-131">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="21371-131">The default value is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21371-132">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="21371-132">-SpecificationFormat</span></span>
<span data-ttu-id="21371-133">Задает формат спецификации.</span><span class="sxs-lookup"><span data-stu-id="21371-133">Specifies the specification format.</span></span>
<span data-ttu-id="21371-134">psdx_paramvalues WADL, WSDL и Swagger.</span><span class="sxs-lookup"><span data-stu-id="21371-134">psdx_paramvalues Wadl, Wsdl, and Swagger.</span></span>

```yaml
Type: PsApiManagementApiFormat
Parameter Sets: (All)
Aliases: 
Accepted values: Wadl, Swagger, Wsdl

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21371-135">-SpecificationPath</span><span class="sxs-lookup"><span data-stu-id="21371-135">-SpecificationPath</span></span>
<span data-ttu-id="21371-136">Задает путь к файлу спецификации.</span><span class="sxs-lookup"><span data-stu-id="21371-136">Specifies the specification file path.</span></span>

```yaml
Type: String
Parameter Sets: ImportFromLocalFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21371-137">-SpecificationUrl</span><span class="sxs-lookup"><span data-stu-id="21371-137">-SpecificationUrl</span></span>
<span data-ttu-id="21371-138">Указывает URL-адрес спецификации.</span><span class="sxs-lookup"><span data-stu-id="21371-138">Specifies the specification URL.</span></span>

```yaml
Type: String
Parameter Sets: ImportFromUrl
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21371-139">-WsdlEndpointName</span><span class="sxs-lookup"><span data-stu-id="21371-139">-WsdlEndpointName</span></span>
<span data-ttu-id="21371-140">Локальное имя конечной точки WSDL (порта), которое нужно импортировать.</span><span class="sxs-lookup"><span data-stu-id="21371-140">Local name of WSDL Endpoint (port) to be imported.</span></span> <span data-ttu-id="21371-141">Должно содержать от 1 до 400 символов.</span><span class="sxs-lookup"><span data-stu-id="21371-141">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="21371-142">Этот параметр является необязательным и требуется только для импорта WSDL.</span><span class="sxs-lookup"><span data-stu-id="21371-142">This parameter is optional and only required for importing Wsdl.</span></span> <span data-ttu-id="21371-143">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="21371-143">Default value is $null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21371-144">-WsdlServiceName</span><span class="sxs-lookup"><span data-stu-id="21371-144">-WsdlServiceName</span></span>
<span data-ttu-id="21371-145">Локальное имя службы WSDL, которую нужно импортировать.</span><span class="sxs-lookup"><span data-stu-id="21371-145">Local name of WSDL Service to be imported.</span></span> <span data-ttu-id="21371-146">Должно содержать от 1 до 400 символов.</span><span class="sxs-lookup"><span data-stu-id="21371-146">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="21371-147">Этот параметр является необязательным и требуется только для импорта WSDL.</span><span class="sxs-lookup"><span data-stu-id="21371-147">This parameter is optional and only required for importing Wsdl .</span></span> <span data-ttu-id="21371-148">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="21371-148">Default value is $null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21371-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21371-149">CommonParameters</span></span>
<span data-ttu-id="21371-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="21371-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21371-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21371-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21371-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="21371-152">INPUTS</span></span>

### <span data-ttu-id="21371-153">Ничего</span><span class="sxs-lookup"><span data-stu-id="21371-153">None</span></span>
<span data-ttu-id="21371-154">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="21371-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="21371-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="21371-155">OUTPUTS</span></span>

### <span data-ttu-id="21371-156">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="21371-156">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="21371-157">Этот командлет возвращает импортированный API как объект **PsApiManagementApi** .</span><span class="sxs-lookup"><span data-stu-id="21371-157">This cmdlet returns the imported API as a **PsApiManagementApi** object.</span></span>

## <span data-ttu-id="21371-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="21371-158">NOTES</span></span>

## <span data-ttu-id="21371-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="21371-159">RELATED LINKS</span></span>

[<span data-ttu-id="21371-160">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="21371-160">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="21371-161">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="21371-161">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="21371-162">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="21371-162">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="21371-163">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="21371-163">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="21371-164">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="21371-164">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


