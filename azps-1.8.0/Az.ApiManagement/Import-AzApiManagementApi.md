---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 48C143BE-3BF6-43E3-99B0-1A1D12A0A3F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/import-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
ms.openlocfilehash: 690ebbfb1bb3cca6de8feb1f199068510e41f1d5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720128"
---
# <span data-ttu-id="f3982-101">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f3982-101">Import-AzApiManagementApi</span></span>

## <span data-ttu-id="f3982-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f3982-102">SYNOPSIS</span></span>
<span data-ttu-id="f3982-103">Импортирует API из файла или URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="f3982-103">Imports an API from a file or a URL.</span></span>

## <span data-ttu-id="f3982-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f3982-104">SYNTAX</span></span>

### <span data-ttu-id="f3982-105">ImportFromLocalFile (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f3982-105">ImportFromLocalFile (Default)</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationPath <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3982-106">ImportFromUrl</span><span class="sxs-lookup"><span data-stu-id="f3982-106">ImportFromUrl</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationUrl <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3982-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3982-107">DESCRIPTION</span></span>
<span data-ttu-id="f3982-108">Командлет **Import-AzApiManagementApi** импортирует API Azure API Management из файла или URL-адреса в языке описания веб-приложений (WADL), языка описания веб-служб (WSDL) или в формате Swagger.</span><span class="sxs-lookup"><span data-stu-id="f3982-108">The **Import-AzApiManagementApi** cmdlet imports an Azure API Management API from a file or a URL in Web Application Description Language (WADL), Web Services Description Language (WSDL), or Swagger format.</span></span>

## <span data-ttu-id="f3982-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f3982-109">EXAMPLES</span></span>

### <span data-ttu-id="f3982-110">Пример 1 Импорт API из файла WADL</span><span class="sxs-lookup"><span data-stu-id="f3982-110">Example 1 Import an API from a WADL file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationPath "C:\contoso\specifications\echoapi.wadl" -Path "apis"
```

<span data-ttu-id="f3982-111">Эта команда импортирует API из указанного файла WADL.</span><span class="sxs-lookup"><span data-stu-id="f3982-111">This command imports an API from the specified WADL file.</span></span>

### <span data-ttu-id="f3982-112">Пример 2. Импорт API из файла Swagger</span><span class="sxs-lookup"><span data-stu-id="f3982-112">Example 2 Import an API from a Swagger file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Swagger" -SpecificationPath "C:\contoso\specifications\echoapi.swagger" -Path "apis"
```

<span data-ttu-id="f3982-113">Эта команда импортирует API из указанного файла Swagger.</span><span class="sxs-lookup"><span data-stu-id="f3982-113">This command imports an API from the specified Swagger file.</span></span>

### <span data-ttu-id="f3982-114">Пример 3: импорт API-интерфейса из ссылки WADL</span><span class="sxs-lookup"><span data-stu-id="f3982-114">Example 3: Import an API from a WADL link</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationUrl "http://contoso.com/specifications/wadl/echoapi" -Path "apis"
```

<span data-ttu-id="f3982-115">Эта команда импортирует API из указанной ссылки WADL.</span><span class="sxs-lookup"><span data-stu-id="f3982-115">This command imports an API from the specified WADL link.</span></span>

## <span data-ttu-id="f3982-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f3982-116">PARAMETERS</span></span>

### <span data-ttu-id="f3982-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="f3982-117">-ApiId</span></span>
<span data-ttu-id="f3982-118">Указывает идентификатор API для импорта.</span><span class="sxs-lookup"><span data-stu-id="f3982-118">Specifies an ID for the API to import.</span></span>
<span data-ttu-id="f3982-119">Если этот параметр не указан, для вас создается идентификатор.</span><span class="sxs-lookup"><span data-stu-id="f3982-119">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="f3982-120">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="f3982-120">-ApiRevision</span></span>
<span data-ttu-id="f3982-121">Идентификатор редакции API.</span><span class="sxs-lookup"><span data-stu-id="f3982-121">Identifier of API Revision.</span></span> <span data-ttu-id="f3982-122">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="f3982-122">This parameter is optional.</span></span> <span data-ttu-id="f3982-123">Если этот элемент не указан, импорт будет выполнен на текущую активную версию или в новый API-интерфейс.</span><span class="sxs-lookup"><span data-stu-id="f3982-123">If not specified, the import will be done onto the currently active revision or a new api.</span></span>

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

### <span data-ttu-id="f3982-124">-ApiType</span><span class="sxs-lookup"><span data-stu-id="f3982-124">-ApiType</span></span>
<span data-ttu-id="f3982-125">Этот параметр является необязательным с использованием значения по умолчанию HTTP.</span><span class="sxs-lookup"><span data-stu-id="f3982-125">This parameter is optional with a default value of Http.</span></span> <span data-ttu-id="f3982-126">Параметр SOAP применим только при импорте WSDL и создаст API-интерфейс для протокола SOAP PassThrough.</span><span class="sxs-lookup"><span data-stu-id="f3982-126">The Soap option is only applicable when importing WSDL and will create a SOAP Passthrough API.</span></span>

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

### <span data-ttu-id="f3982-127">-Context</span><span class="sxs-lookup"><span data-stu-id="f3982-127">-Context</span></span>
<span data-ttu-id="f3982-128">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="f3982-128">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f3982-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3982-129">-DefaultProfile</span></span>
<span data-ttu-id="f3982-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f3982-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3982-131">-Path</span><span class="sxs-lookup"><span data-stu-id="f3982-131">-Path</span></span>
<span data-ttu-id="f3982-132">Указывает путь веб-API как последнюю часть общедоступного URL-адреса API.</span><span class="sxs-lookup"><span data-stu-id="f3982-132">Specifies a web API path as the last part of the API's public URL.</span></span>
<span data-ttu-id="f3982-133">Этот URL-адрес используется клиентами API для отправки запросов на веб-службу.</span><span class="sxs-lookup"><span data-stu-id="f3982-133">This URL is used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="f3982-134">Должно содержать от 1 до 400 символов.</span><span class="sxs-lookup"><span data-stu-id="f3982-134">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="f3982-135">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="f3982-135">The default value is $Null.</span></span>

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

### <span data-ttu-id="f3982-136">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="f3982-136">-SpecificationFormat</span></span>
<span data-ttu-id="f3982-137">Задает формат спецификации.</span><span class="sxs-lookup"><span data-stu-id="f3982-137">Specifies the specification format.</span></span>
<span data-ttu-id="f3982-138">psdx_paramvalues WADL, WSDL и Swagger.</span><span class="sxs-lookup"><span data-stu-id="f3982-138">psdx_paramvalues Wadl, Wsdl, and Swagger.</span></span>

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

### <span data-ttu-id="f3982-139">-SpecificationPath</span><span class="sxs-lookup"><span data-stu-id="f3982-139">-SpecificationPath</span></span>
<span data-ttu-id="f3982-140">Задает путь к файлу спецификации.</span><span class="sxs-lookup"><span data-stu-id="f3982-140">Specifies the specification file path.</span></span>

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

### <span data-ttu-id="f3982-141">-SpecificationUrl</span><span class="sxs-lookup"><span data-stu-id="f3982-141">-SpecificationUrl</span></span>
<span data-ttu-id="f3982-142">Указывает URL-адрес спецификации.</span><span class="sxs-lookup"><span data-stu-id="f3982-142">Specifies the specification URL.</span></span>

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

### <span data-ttu-id="f3982-143">-WsdlEndpointName</span><span class="sxs-lookup"><span data-stu-id="f3982-143">-WsdlEndpointName</span></span>
<span data-ttu-id="f3982-144">Локальное имя конечной точки WSDL (порта), которое нужно импортировать.</span><span class="sxs-lookup"><span data-stu-id="f3982-144">Local name of WSDL Endpoint (port) to be imported.</span></span> <span data-ttu-id="f3982-145">Должно содержать от 1 до 400 символов.</span><span class="sxs-lookup"><span data-stu-id="f3982-145">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="f3982-146">Этот параметр является необязательным и требуется только для импорта WSDL.</span><span class="sxs-lookup"><span data-stu-id="f3982-146">This parameter is optional and only required for importing Wsdl.</span></span> <span data-ttu-id="f3982-147">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="f3982-147">Default value is $null.</span></span>

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

### <span data-ttu-id="f3982-148">-WsdlServiceName</span><span class="sxs-lookup"><span data-stu-id="f3982-148">-WsdlServiceName</span></span>
<span data-ttu-id="f3982-149">Локальное имя службы WSDL, которую нужно импортировать.</span><span class="sxs-lookup"><span data-stu-id="f3982-149">Local name of WSDL Service to be imported.</span></span> <span data-ttu-id="f3982-150">Должно содержать от 1 до 400 символов.</span><span class="sxs-lookup"><span data-stu-id="f3982-150">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="f3982-151">Этот параметр является необязательным и требуется только для импорта WSDL.</span><span class="sxs-lookup"><span data-stu-id="f3982-151">This parameter is optional and only required for importing Wsdl .</span></span> <span data-ttu-id="f3982-152">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="f3982-152">Default value is $null.</span></span>

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

### <span data-ttu-id="f3982-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3982-153">CommonParameters</span></span>
<span data-ttu-id="f3982-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f3982-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3982-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3982-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3982-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f3982-156">INPUTS</span></span>

### <span data-ttu-id="f3982-157">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f3982-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f3982-158">System. String</span><span class="sxs-lookup"><span data-stu-id="f3982-158">System.String</span></span>

### <span data-ttu-id="f3982-159">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="f3982-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="f3982-160">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. ServiceManagement.. PsApiManagementApiType, Microsoft. Azure. PowerShell. командлеты. ApiManagement. ServiceManagement, Version = 1.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="f3982-160">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiType, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f3982-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3982-161">OUTPUTS</span></span>

### <span data-ttu-id="f3982-162">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f3982-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="f3982-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="f3982-163">NOTES</span></span>

## <span data-ttu-id="f3982-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f3982-164">RELATED LINKS</span></span>

[<span data-ttu-id="f3982-165">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f3982-165">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="f3982-166">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f3982-166">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="f3982-167">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f3982-167">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="f3982-168">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f3982-168">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="f3982-169">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f3982-169">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


