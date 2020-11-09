---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementPolicy.md
ms.openlocfilehash: 24af453d6605bc42e8c504cef26d368369753d9d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318149"
---
# <span data-ttu-id="4a0ab-101">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="4a0ab-101">Get-AzApiManagementPolicy</span></span>

## <span data-ttu-id="4a0ab-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4a0ab-102">SYNOPSIS</span></span>
<span data-ttu-id="4a0ab-103">Получает указанную политику области.</span><span class="sxs-lookup"><span data-stu-id="4a0ab-103">Gets the specified scope policy.</span></span>

## <span data-ttu-id="4a0ab-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4a0ab-104">SYNTAX</span></span>

### <span data-ttu-id="4a0ab-105">GetTenantLevel (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4a0ab-105">GetTenantLevel (Default)</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a0ab-106">GetProductLevel</span><span class="sxs-lookup"><span data-stu-id="4a0ab-106">GetProductLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4a0ab-107">GetApiLevel</span><span class="sxs-lookup"><span data-stu-id="4a0ab-107">GetApiLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a0ab-108">GetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="4a0ab-108">GetOperationLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] -OperationId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a0ab-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a0ab-109">DESCRIPTION</span></span>
<span data-ttu-id="4a0ab-110">Командлет **Get-AzApiManagementPolicy** получает указанную политику области.</span><span class="sxs-lookup"><span data-stu-id="4a0ab-110">The **Get-AzApiManagementPolicy** cmdlet gets the specified scope policy.</span></span>

## <span data-ttu-id="4a0ab-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4a0ab-111">EXAMPLES</span></span>

### <span data-ttu-id="4a0ab-112">Пример 1: получение политики уровня клиента</span><span class="sxs-lookup"><span data-stu-id="4a0ab-112">Example 1: Get the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="4a0ab-113">Эта команда получает политику уровня клиента и сохраняет ее в файле с именем tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="4a0ab-113">This command gets tenant level policy and saves it to a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="4a0ab-114">Пример 2: получение политики для области продукта</span><span class="sxs-lookup"><span data-stu-id="4a0ab-114">Example 2: Get the product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="4a0ab-115">Эта команда получает политику области продукта</span><span class="sxs-lookup"><span data-stu-id="4a0ab-115">This command gets product-scope policy</span></span>

### <span data-ttu-id="4a0ab-116">Пример 3: получение политики области API</span><span class="sxs-lookup"><span data-stu-id="4a0ab-116">Example 3: Get the API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="4a0ab-117">Эта команда получает политику области API.</span><span class="sxs-lookup"><span data-stu-id="4a0ab-117">This command gets API-scope policy.</span></span>

### <span data-ttu-id="4a0ab-118">Пример 4: получение политики области действия для операции</span><span class="sxs-lookup"><span data-stu-id="4a0ab-118">Example 4: Get the operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="4a0ab-119">Эта команда получает политику области действия.</span><span class="sxs-lookup"><span data-stu-id="4a0ab-119">This command gets the operation-scope policy.</span></span>

### <span data-ttu-id="4a0ab-120">Пример 5: получение политики области клиента в формате RawXml</span><span class="sxs-lookup"><span data-stu-id="4a0ab-120">Example 5: Get the Tenant scope policy in RawXml format</span></span>
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

<span data-ttu-id="4a0ab-121">Эта команда возвращает политику области клиента в формате, отличном от XML-формата.</span><span class="sxs-lookup"><span data-stu-id="4a0ab-121">This command gets the tenant-scope policy in Non-Xml escaped format.</span></span>

## <span data-ttu-id="4a0ab-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4a0ab-122">PARAMETERS</span></span>

### <span data-ttu-id="4a0ab-123">-ApiId</span><span class="sxs-lookup"><span data-stu-id="4a0ab-123">-ApiId</span></span>
<span data-ttu-id="4a0ab-124">Указывает идентификатор существующего API.</span><span class="sxs-lookup"><span data-stu-id="4a0ab-124">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="4a0ab-125">Если указать этот параметр, командлет возвращает политику области API.</span><span class="sxs-lookup"><span data-stu-id="4a0ab-125">If you specify this parameter the cmdlet returns the API-scope policy.</span></span>

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

### <span data-ttu-id="4a0ab-126">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="4a0ab-126">-ApiRevision</span></span>
<span data-ttu-id="4a0ab-127">Идентификатор редакции API.</span><span class="sxs-lookup"><span data-stu-id="4a0ab-127">Identifier of API Revision.</span></span> <span data-ttu-id="4a0ab-128">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="4a0ab-128">This parameter is optional.</span></span> <span data-ttu-id="4a0ab-129">Если не указано, политика будет получена из текущей активной версии API.</span><span class="sxs-lookup"><span data-stu-id="4a0ab-129">If not specified, the policy will be retrieved from the currently active api revision.</span></span>

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

### <span data-ttu-id="4a0ab-130">-Context</span><span class="sxs-lookup"><span data-stu-id="4a0ab-130">-Context</span></span>
<span data-ttu-id="4a0ab-131">Указывает экземпляр **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="4a0ab-131">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="4a0ab-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a0ab-132">-DefaultProfile</span></span>
<span data-ttu-id="4a0ab-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4a0ab-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a0ab-134">-Force</span><span class="sxs-lookup"><span data-stu-id="4a0ab-134">-Force</span></span>
<span data-ttu-id="4a0ab-135">ps_force</span><span class="sxs-lookup"><span data-stu-id="4a0ab-135">ps_force</span></span>

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

### <span data-ttu-id="4a0ab-136">-Format</span><span class="sxs-lookup"><span data-stu-id="4a0ab-136">-Format</span></span>
<span data-ttu-id="4a0ab-137">Задает формат политики управления API.</span><span class="sxs-lookup"><span data-stu-id="4a0ab-137">Specifies the format of the API management policy.</span></span>
<span data-ttu-id="4a0ab-138">Значением по умолчанию для этого параметра является XML.</span><span class="sxs-lookup"><span data-stu-id="4a0ab-138">The default value for this parameter is "xml".</span></span>

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

### <span data-ttu-id="4a0ab-139">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="4a0ab-139">-OperationId</span></span>
<span data-ttu-id="4a0ab-140">Указывает идентификатор существующей операции API.</span><span class="sxs-lookup"><span data-stu-id="4a0ab-140">Specifies the identifier of the existing API operation.</span></span>
<span data-ttu-id="4a0ab-141">Если указать этот параметр в *ApiId* , командлет возвращает политику области действия.</span><span class="sxs-lookup"><span data-stu-id="4a0ab-141">If you specify this parameter with *ApiId* the cmdlet returns operation-scope policy.</span></span>

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

### <span data-ttu-id="4a0ab-142">-ProductId</span><span class="sxs-lookup"><span data-stu-id="4a0ab-142">-ProductId</span></span>
<span data-ttu-id="4a0ab-143">Указывает идентификатор существующего продукта.</span><span class="sxs-lookup"><span data-stu-id="4a0ab-143">Specifies the identifier of an existing product.</span></span>
<span data-ttu-id="4a0ab-144">Если указать этот параметр, командлет возвращает политику области продукта.</span><span class="sxs-lookup"><span data-stu-id="4a0ab-144">If you specify this parameter the cmdlet returns the product-scope policy.</span></span>

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

### <span data-ttu-id="4a0ab-145">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="4a0ab-145">-SaveAs</span></span>
<span data-ttu-id="4a0ab-146">Задает путь к файлу, в который нужно сохранить результат.</span><span class="sxs-lookup"><span data-stu-id="4a0ab-146">Specifies the file path to save the result to.</span></span>
<span data-ttu-id="4a0ab-147">Если этот параметр не указан, результат будет конвейерная, как Sting.</span><span class="sxs-lookup"><span data-stu-id="4a0ab-147">If you do not specify this parameter the result is pipelined as a sting.</span></span>

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

### <span data-ttu-id="4a0ab-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4a0ab-148">-Confirm</span></span>
<span data-ttu-id="4a0ab-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4a0ab-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a0ab-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a0ab-150">-WhatIf</span></span>
<span data-ttu-id="4a0ab-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4a0ab-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4a0ab-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4a0ab-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a0ab-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a0ab-153">CommonParameters</span></span>
<span data-ttu-id="4a0ab-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4a0ab-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a0ab-155">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a0ab-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a0ab-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4a0ab-156">INPUTS</span></span>

### <span data-ttu-id="4a0ab-157">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4a0ab-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4a0ab-158">System. String</span><span class="sxs-lookup"><span data-stu-id="4a0ab-158">System.String</span></span>

### <span data-ttu-id="4a0ab-159">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4a0ab-159">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4a0ab-160">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a0ab-160">OUTPUTS</span></span>

### <span data-ttu-id="4a0ab-161">System. String</span><span class="sxs-lookup"><span data-stu-id="4a0ab-161">System.String</span></span>

## <span data-ttu-id="4a0ab-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="4a0ab-162">NOTES</span></span>

## <span data-ttu-id="4a0ab-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4a0ab-163">RELATED LINKS</span></span>

[<span data-ttu-id="4a0ab-164">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="4a0ab-164">Remove-AzApiManagementPolicy</span></span>](./Remove-AzApiManagementPolicy.md)

[<span data-ttu-id="4a0ab-165">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="4a0ab-165">Set-AzApiManagementPolicy</span></span>](./Set-AzApiManagementPolicy.md)


