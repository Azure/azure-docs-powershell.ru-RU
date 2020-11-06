---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 48C143BE-3BF6-43E3-99B0-1A1D12A0A3F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/import-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementApi.md
ms.openlocfilehash: 7eb2e25f137abb303e1c9fa5b4ebe8b932346871
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563183"
---
# <span data-ttu-id="418f7-101">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="418f7-101">Import-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="418f7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="418f7-102">SYNOPSIS</span></span>
<span data-ttu-id="418f7-103">Импортирует API из файла или URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="418f7-103">Imports an API from a file or a URL.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="418f7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="418f7-104">SYNTAX</span></span>

### <span data-ttu-id="418f7-105">ImportFromLocalFile (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="418f7-105">ImportFromLocalFile (Default)</span></span>
```
Import-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationPath <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="418f7-106">ImportFromUrl</span><span class="sxs-lookup"><span data-stu-id="418f7-106">ImportFromUrl</span></span>
```
Import-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationUrl <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="418f7-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="418f7-107">DESCRIPTION</span></span>
<span data-ttu-id="418f7-108">Командлет **Import-AzureRmApiManagementApi** импортирует API Azure API Management из файла или URL-адреса в языке описания веб-приложений (WADL), языка описания веб-служб (WSDL) или в формате Swagger.</span><span class="sxs-lookup"><span data-stu-id="418f7-108">The **Import-AzureRmApiManagementApi** cmdlet imports an Azure API Management API from a file or a URL in Web Application Description Language (WADL), Web Services Description Language (WSDL), or Swagger format.</span></span>

## <span data-ttu-id="418f7-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="418f7-109">EXAMPLES</span></span>

### <span data-ttu-id="418f7-110">Пример 1 Импорт API из файла WADL</span><span class="sxs-lookup"><span data-stu-id="418f7-110">Example 1 Import an API from a WADL file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationPath "C:\contoso\specifications\echoapi.wadl" -Path "apis"
```

<span data-ttu-id="418f7-111">Эта команда импортирует API из указанного файла WADL.</span><span class="sxs-lookup"><span data-stu-id="418f7-111">This command imports an API from the specified WADL file.</span></span>

### <span data-ttu-id="418f7-112">Пример 2. Импорт API из файла Swagger</span><span class="sxs-lookup"><span data-stu-id="418f7-112">Example 2 Import an API from a Swagger file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Swagger" -SpecificationPath "C:\contoso\specifications\echoapi.swagger" -Path "apis"
```

<span data-ttu-id="418f7-113">Эта команда импортирует API из указанного файла Swagger.</span><span class="sxs-lookup"><span data-stu-id="418f7-113">This command imports an API from the specified Swagger file.</span></span>

### <span data-ttu-id="418f7-114">Пример 3: импорт API-интерфейса из ссылки WADL</span><span class="sxs-lookup"><span data-stu-id="418f7-114">Example 3: Import an API from a WADL link</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationUrl "http://contoso.com/specifications/wadl/echoapi" -Path "apis"
```

<span data-ttu-id="418f7-115">Эта команда импортирует API из указанной ссылки WADL.</span><span class="sxs-lookup"><span data-stu-id="418f7-115">This command imports an API from the specified WADL link.</span></span>

## <span data-ttu-id="418f7-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="418f7-116">PARAMETERS</span></span>

### <span data-ttu-id="418f7-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="418f7-117">-ApiId</span></span>
<span data-ttu-id="418f7-118">Указывает идентификатор API для импорта.</span><span class="sxs-lookup"><span data-stu-id="418f7-118">Specifies an ID for the API to import.</span></span>
<span data-ttu-id="418f7-119">Если этот параметр не указан, для вас создается идентификатор.</span><span class="sxs-lookup"><span data-stu-id="418f7-119">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="418f7-120">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="418f7-120">-ApiRevision</span></span>
<span data-ttu-id="418f7-121">Идентификатор редакции API.</span><span class="sxs-lookup"><span data-stu-id="418f7-121">Identifier of API Revision.</span></span> <span data-ttu-id="418f7-122">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="418f7-122">This parameter is optional.</span></span> <span data-ttu-id="418f7-123">Если этот элемент не указан, импорт будет выполнен на текущую активную версию или в новый API-интерфейс.</span><span class="sxs-lookup"><span data-stu-id="418f7-123">If not specified, the import will be done onto the currently active revision or a new api.</span></span>

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

### <span data-ttu-id="418f7-124">-ApiType</span><span class="sxs-lookup"><span data-stu-id="418f7-124">-ApiType</span></span>
<span data-ttu-id="418f7-125">Этот параметр является необязательным с использованием значения по умолчанию HTTP.</span><span class="sxs-lookup"><span data-stu-id="418f7-125">This parameter is optional with a default value of Http.</span></span> <span data-ttu-id="418f7-126">Параметр SOAP применим только при импорте WSDL и создаст API-интерфейс для протокола SOAP PassThrough.</span><span class="sxs-lookup"><span data-stu-id="418f7-126">The Soap option is only applicable when importing WSDL and will create a SOAP Passthrough API.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiType]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Soap

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="418f7-127">-Context</span><span class="sxs-lookup"><span data-stu-id="418f7-127">-Context</span></span>
<span data-ttu-id="418f7-128">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="418f7-128">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="418f7-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="418f7-129">-DefaultProfile</span></span>
<span data-ttu-id="418f7-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="418f7-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="418f7-131">-Path</span><span class="sxs-lookup"><span data-stu-id="418f7-131">-Path</span></span>
<span data-ttu-id="418f7-132">Указывает путь веб-API как последнюю часть общедоступного URL-адреса API.</span><span class="sxs-lookup"><span data-stu-id="418f7-132">Specifies a web API path as the last part of the API's public URL.</span></span>
<span data-ttu-id="418f7-133">Этот URL-адрес используется клиентами API для отправки запросов на веб-службу.</span><span class="sxs-lookup"><span data-stu-id="418f7-133">This URL is used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="418f7-134">Должно содержать от 1 до 400 символов.</span><span class="sxs-lookup"><span data-stu-id="418f7-134">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="418f7-135">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="418f7-135">The default value is $Null.</span></span>

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

### <span data-ttu-id="418f7-136">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="418f7-136">-SpecificationFormat</span></span>
<span data-ttu-id="418f7-137">Задает формат спецификации.</span><span class="sxs-lookup"><span data-stu-id="418f7-137">Specifies the specification format.</span></span>
<span data-ttu-id="418f7-138">psdx_paramvalues WADL, WSDL и Swagger.</span><span class="sxs-lookup"><span data-stu-id="418f7-138">psdx_paramvalues Wadl, Wsdl, and Swagger.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat
Parameter Sets: (All)
Aliases:
Accepted values: Wadl, Swagger, Wsdl

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="418f7-139">-SpecificationPath</span><span class="sxs-lookup"><span data-stu-id="418f7-139">-SpecificationPath</span></span>
<span data-ttu-id="418f7-140">Задает путь к файлу спецификации.</span><span class="sxs-lookup"><span data-stu-id="418f7-140">Specifies the specification file path.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromLocalFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="418f7-141">-SpecificationUrl</span><span class="sxs-lookup"><span data-stu-id="418f7-141">-SpecificationUrl</span></span>
<span data-ttu-id="418f7-142">Указывает URL-адрес спецификации.</span><span class="sxs-lookup"><span data-stu-id="418f7-142">Specifies the specification URL.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="418f7-143">-WsdlEndpointName</span><span class="sxs-lookup"><span data-stu-id="418f7-143">-WsdlEndpointName</span></span>
<span data-ttu-id="418f7-144">Локальное имя конечной точки WSDL (порта), которое нужно импортировать.</span><span class="sxs-lookup"><span data-stu-id="418f7-144">Local name of WSDL Endpoint (port) to be imported.</span></span> <span data-ttu-id="418f7-145">Должно содержать от 1 до 400 символов.</span><span class="sxs-lookup"><span data-stu-id="418f7-145">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="418f7-146">Этот параметр является необязательным и требуется только для импорта WSDL.</span><span class="sxs-lookup"><span data-stu-id="418f7-146">This parameter is optional and only required for importing Wsdl.</span></span> <span data-ttu-id="418f7-147">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="418f7-147">Default value is $null.</span></span>

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

### <span data-ttu-id="418f7-148">-WsdlServiceName</span><span class="sxs-lookup"><span data-stu-id="418f7-148">-WsdlServiceName</span></span>
<span data-ttu-id="418f7-149">Локальное имя службы WSDL, которую нужно импортировать.</span><span class="sxs-lookup"><span data-stu-id="418f7-149">Local name of WSDL Service to be imported.</span></span> <span data-ttu-id="418f7-150">Должно содержать от 1 до 400 символов.</span><span class="sxs-lookup"><span data-stu-id="418f7-150">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="418f7-151">Этот параметр является необязательным и требуется только для импорта WSDL.</span><span class="sxs-lookup"><span data-stu-id="418f7-151">This parameter is optional and only required for importing Wsdl .</span></span> <span data-ttu-id="418f7-152">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="418f7-152">Default value is $null.</span></span>

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

### <span data-ttu-id="418f7-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="418f7-153">CommonParameters</span></span>
<span data-ttu-id="418f7-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="418f7-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="418f7-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="418f7-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="418f7-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="418f7-156">INPUTS</span></span>

### <span data-ttu-id="418f7-157">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="418f7-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="418f7-158">System. String</span><span class="sxs-lookup"><span data-stu-id="418f7-158">System.String</span></span>

### <span data-ttu-id="418f7-159">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="418f7-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="418f7-160">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiType, Microsoft. Azure. Commands. ApiManagement. ServiceManagement, Version = 6.1.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="418f7-160">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiType, Microsoft.Azure.Commands.ApiManagement.ServiceManagement, Version=6.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="418f7-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="418f7-161">OUTPUTS</span></span>

### <span data-ttu-id="418f7-162">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="418f7-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="418f7-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="418f7-163">NOTES</span></span>

## <span data-ttu-id="418f7-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="418f7-164">RELATED LINKS</span></span>

[<span data-ttu-id="418f7-165">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="418f7-165">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="418f7-166">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="418f7-166">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="418f7-167">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="418f7-167">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="418f7-168">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="418f7-168">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="418f7-169">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="418f7-169">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


