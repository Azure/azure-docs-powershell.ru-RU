---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementPolicy.md
ms.openlocfilehash: 24af453d6605bc42e8c504cef26d368369753d9d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100221793"
---
# <span data-ttu-id="3c88f-101">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="3c88f-101">Get-AzApiManagementPolicy</span></span>

## <span data-ttu-id="3c88f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c88f-102">SYNOPSIS</span></span>
<span data-ttu-id="3c88f-103">Получает указанную политику области.</span><span class="sxs-lookup"><span data-stu-id="3c88f-103">Gets the specified scope policy.</span></span>

## <span data-ttu-id="3c88f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3c88f-104">SYNTAX</span></span>

### <span data-ttu-id="3c88f-105">GetTenantLevel (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3c88f-105">GetTenantLevel (Default)</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c88f-106">GetProductLevel</span><span class="sxs-lookup"><span data-stu-id="3c88f-106">GetProductLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3c88f-107">GetApiLevel</span><span class="sxs-lookup"><span data-stu-id="3c88f-107">GetApiLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c88f-108">GetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="3c88f-108">GetOperationLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] -OperationId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c88f-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c88f-109">DESCRIPTION</span></span>
<span data-ttu-id="3c88f-110">Заданную политику области **получает cmdlet Get-AzApiManagementPolicy.**</span><span class="sxs-lookup"><span data-stu-id="3c88f-110">The **Get-AzApiManagementPolicy** cmdlet gets the specified scope policy.</span></span>

## <span data-ttu-id="3c88f-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3c88f-111">EXAMPLES</span></span>

### <span data-ttu-id="3c88f-112">Пример 1. Получить политику на уровне клиента</span><span class="sxs-lookup"><span data-stu-id="3c88f-112">Example 1: Get the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="3c88f-113">Эта команда получает политику на уровне клиента и сохраняет ее в файл с tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="3c88f-113">This command gets tenant level policy and saves it to a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="3c88f-114">Пример 2. Получить политику области продуктов</span><span class="sxs-lookup"><span data-stu-id="3c88f-114">Example 2: Get the product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="3c88f-115">Эта команда получает политику области продуктов</span><span class="sxs-lookup"><span data-stu-id="3c88f-115">This command gets product-scope policy</span></span>

### <span data-ttu-id="3c88f-116">Пример 3. Получить политику области API</span><span class="sxs-lookup"><span data-stu-id="3c88f-116">Example 3: Get the API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="3c88f-117">Эта команда получает политику области API.</span><span class="sxs-lookup"><span data-stu-id="3c88f-117">This command gets API-scope policy.</span></span>

### <span data-ttu-id="3c88f-118">Пример 4. Просмотр политики области действия</span><span class="sxs-lookup"><span data-stu-id="3c88f-118">Example 4: Get the operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="3c88f-119">Эта команда получает политику области действия.</span><span class="sxs-lookup"><span data-stu-id="3c88f-119">This command gets the operation-scope policy.</span></span>

### <span data-ttu-id="3c88f-120">Пример 5. Просмотр политики области клиента в формате RawXml</span><span class="sxs-lookup"><span data-stu-id="3c88f-120">Example 5: Get the Tenant scope policy in RawXml format</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS c:\> Get-AzApiManagementPolicy -Context $apimContext -Format rawxml

<policies>
        <inbound>
                <set-header name="correlationid" exists-action="skip">
                        <value>@{
                var guidBinary = new byte[16];
                Array.Copy(Guid.NewGuid().ToByteArray(), 0, guidBinary, 0, 10);
                long time = DateTime.Now.Ticks;
                byte[] bytes = new byte[6];
                unchecked
                {
                       bytes[5] = (byte)(time >> 40);
                       bytes[4] = (byte)(time >> 32);
                       bytes[3] = (byte)(time >> 24);
                       bytes[2] = (byte)(time >> 16);
                       bytes[1] = (byte)(time >> 8);
                       bytes[0] = (byte)(time);
                }
                Array.Copy(bytes, 0, guidBinary, 10, 6);
                return new Guid(guidBinary).ToString();
            }
            </value>
                </set-header>
        </inbound>
        <backend>
                <forward-request />
        </backend>
        <outbound />
        <on-error />
</policies>
```

<span data-ttu-id="3c88f-121">Эта команда получает политику на область клиента в escape-формате non-XML.</span><span class="sxs-lookup"><span data-stu-id="3c88f-121">This command gets the tenant-scope policy in Non-Xml escaped format.</span></span>

## <span data-ttu-id="3c88f-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c88f-122">PARAMETERS</span></span>

### <span data-ttu-id="3c88f-123">-ApiId</span><span class="sxs-lookup"><span data-stu-id="3c88f-123">-ApiId</span></span>
<span data-ttu-id="3c88f-124">Указывает идентификатор существующего API.</span><span class="sxs-lookup"><span data-stu-id="3c88f-124">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="3c88f-125">Если этот параметр задан, будет возвращена политика области API.</span><span class="sxs-lookup"><span data-stu-id="3c88f-125">If you specify this parameter the cmdlet returns the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c88f-126">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="3c88f-126">-ApiRevision</span></span>
<span data-ttu-id="3c88f-127">Идентификатор изменения API.</span><span class="sxs-lookup"><span data-stu-id="3c88f-127">Identifier of API Revision.</span></span> <span data-ttu-id="3c88f-128">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="3c88f-128">This parameter is optional.</span></span> <span data-ttu-id="3c88f-129">Если не указано, политика будет извлечена из активной редакции API.</span><span class="sxs-lookup"><span data-stu-id="3c88f-129">If not specified, the policy will be retrieved from the currently active api revision.</span></span>

```yaml
Type: System.String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c88f-130">-Контекст</span><span class="sxs-lookup"><span data-stu-id="3c88f-130">-Context</span></span>
<span data-ttu-id="3c88f-131">Указывает экземпляр **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="3c88f-131">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="3c88f-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c88f-132">-DefaultProfile</span></span>
<span data-ttu-id="3c88f-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3c88f-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c88f-134">-Force</span><span class="sxs-lookup"><span data-stu-id="3c88f-134">-Force</span></span>
<span data-ttu-id="3c88f-135">ps_force</span><span class="sxs-lookup"><span data-stu-id="3c88f-135">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c88f-136">-Format</span><span class="sxs-lookup"><span data-stu-id="3c88f-136">-Format</span></span>
<span data-ttu-id="3c88f-137">Формат политики управления API.</span><span class="sxs-lookup"><span data-stu-id="3c88f-137">Specifies the format of the API management policy.</span></span>
<span data-ttu-id="3c88f-138">По умолчанию этот параметр имеет значение XML.</span><span class="sxs-lookup"><span data-stu-id="3c88f-138">The default value for this parameter is "xml".</span></span>

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

### <span data-ttu-id="3c88f-139">-OperationId</span><span class="sxs-lookup"><span data-stu-id="3c88f-139">-OperationId</span></span>
<span data-ttu-id="3c88f-140">Указывает идентификатор существующей операции API.</span><span class="sxs-lookup"><span data-stu-id="3c88f-140">Specifies the identifier of the existing API operation.</span></span>
<span data-ttu-id="3c88f-141">Если для параметра *ApiId* задан этот параметр, возвращается политика области операций.</span><span class="sxs-lookup"><span data-stu-id="3c88f-141">If you specify this parameter with *ApiId* the cmdlet returns operation-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c88f-142">-ProductId</span><span class="sxs-lookup"><span data-stu-id="3c88f-142">-ProductId</span></span>
<span data-ttu-id="3c88f-143">Определяет идентификатор существующего продукта.</span><span class="sxs-lookup"><span data-stu-id="3c88f-143">Specifies the identifier of an existing product.</span></span>
<span data-ttu-id="3c88f-144">Если этот параметр задан, будет возвращена политика области продуктов.</span><span class="sxs-lookup"><span data-stu-id="3c88f-144">If you specify this parameter the cmdlet returns the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetProductLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c88f-145">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="3c88f-145">-SaveAs</span></span>
<span data-ttu-id="3c88f-146">Путь к файлу, в который нужно сохранить результат.</span><span class="sxs-lookup"><span data-stu-id="3c88f-146">Specifies the file path to save the result to.</span></span>
<span data-ttu-id="3c88f-147">Если этот параметр не указан, результат будет отсве речь идет о sting.</span><span class="sxs-lookup"><span data-stu-id="3c88f-147">If you do not specify this parameter the result is pipelined as a sting.</span></span>

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

### <span data-ttu-id="3c88f-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3c88f-148">-Confirm</span></span>
<span data-ttu-id="3c88f-149">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c88f-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c88f-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c88f-150">-WhatIf</span></span>
<span data-ttu-id="3c88f-151">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c88f-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3c88f-152">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3c88f-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c88f-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c88f-153">CommonParameters</span></span>
<span data-ttu-id="3c88f-154">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c88f-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c88f-155">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3c88f-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c88f-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3c88f-156">INPUTS</span></span>

### <span data-ttu-id="3c88f-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3c88f-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3c88f-158">System.String</span><span class="sxs-lookup"><span data-stu-id="3c88f-158">System.String</span></span>

### <span data-ttu-id="3c88f-159">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3c88f-159">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3c88f-160">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3c88f-160">OUTPUTS</span></span>

### <span data-ttu-id="3c88f-161">System.String</span><span class="sxs-lookup"><span data-stu-id="3c88f-161">System.String</span></span>

## <span data-ttu-id="3c88f-162">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3c88f-162">NOTES</span></span>

## <span data-ttu-id="3c88f-163">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3c88f-163">RELATED LINKS</span></span>

[<span data-ttu-id="3c88f-164">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="3c88f-164">Remove-AzApiManagementPolicy</span></span>](./Remove-AzApiManagementPolicy.md)

[<span data-ttu-id="3c88f-165">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="3c88f-165">Set-AzApiManagementPolicy</span></span>](./Set-AzApiManagementPolicy.md)


