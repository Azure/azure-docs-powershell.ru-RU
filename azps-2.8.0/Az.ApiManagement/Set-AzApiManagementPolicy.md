---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementPolicy.md
ms.openlocfilehash: 7398687bed785b0152b991656baf2784df204ed6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727927"
---
# <span data-ttu-id="0f4d3-101">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0f4d3-101">Set-AzApiManagementPolicy</span></span>

## <span data-ttu-id="0f4d3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0f4d3-102">SYNOPSIS</span></span>
<span data-ttu-id="0f4d3-103">Задает указанную политику области для управления API.</span><span class="sxs-lookup"><span data-stu-id="0f4d3-103">Sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="0f4d3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0f4d3-104">SYNTAX</span></span>

### <span data-ttu-id="0f4d3-105">SetTenantLevel (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0f4d3-105">SetTenantLevel (Default)</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0f4d3-106">SetProductLevel</span><span class="sxs-lookup"><span data-stu-id="0f4d3-106">SetProductLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f4d3-107">SetApiLevel</span><span class="sxs-lookup"><span data-stu-id="0f4d3-107">SetApiLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f4d3-108">SetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="0f4d3-108">SetOperationLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>]
 [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f4d3-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f4d3-109">DESCRIPTION</span></span>
<span data-ttu-id="0f4d3-110">Командлет **Set-AzApiManagementPolicy** задает указанную политику области для управления API.</span><span class="sxs-lookup"><span data-stu-id="0f4d3-110">The **Set-AzApiManagementPolicy** cmdlet sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="0f4d3-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0f4d3-111">EXAMPLES</span></span>

### <span data-ttu-id="0f4d3-112">Пример 1: Настройка политики уровня клиента</span><span class="sxs-lookup"><span data-stu-id="0f4d3-112">Example 1: Set the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="0f4d3-113">Эта команда задает политику уровня клиента из файла с именем tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="0f4d3-113">This command sets the tenant level policy from a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="0f4d3-114">Пример 2: Настройка политики для области продукта</span><span class="sxs-lookup"><span data-stu-id="0f4d3-114">Example 2: Set a product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789" -Policy $PolicyString
```

<span data-ttu-id="0f4d3-115">Эта команда задает политику области продукта для управления API.</span><span class="sxs-lookup"><span data-stu-id="0f4d3-115">This command sets the product-scope policy for API Management.</span></span>

### <span data-ttu-id="0f4d3-116">Пример 3: Настройка политики области API</span><span class="sxs-lookup"><span data-stu-id="0f4d3-116">Example 3: Set API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -Policy $PolicyString
```

<span data-ttu-id="0f4d3-117">Эта команда задает политику области API для управления API.</span><span class="sxs-lookup"><span data-stu-id="0f4d3-117">This command sets API-scope policy for API Management.</span></span>

### <span data-ttu-id="0f4d3-118">Пример 4: Настройка политики области действия</span><span class="sxs-lookup"><span data-stu-id="0f4d3-118">Example 4: Set operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

<span data-ttu-id="0f4d3-119">Эта команда задает политику области действия для управления API.</span><span class="sxs-lookup"><span data-stu-id="0f4d3-119">This command sets operation-scope policy for API Management.</span></span>

## <span data-ttu-id="0f4d3-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0f4d3-120">PARAMETERS</span></span>

### <span data-ttu-id="0f4d3-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="0f4d3-121">-ApiId</span></span>
<span data-ttu-id="0f4d3-122">Указывает идентификатор существующего API.</span><span class="sxs-lookup"><span data-stu-id="0f4d3-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="0f4d3-123">Если указать этот параметр, командлет задает политику области API.</span><span class="sxs-lookup"><span data-stu-id="0f4d3-123">If you specify this parameter, the cmdlet sets the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: SetApiLevel, SetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f4d3-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="0f4d3-124">-ApiRevision</span></span>
<span data-ttu-id="0f4d3-125">Идентификатор редакции API.</span><span class="sxs-lookup"><span data-stu-id="0f4d3-125">Identifier of API Revision.</span></span> <span data-ttu-id="0f4d3-126">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="0f4d3-126">This parameter is optional.</span></span> <span data-ttu-id="0f4d3-127">Если не указано, политика будет обновляться в текущей версии API.</span><span class="sxs-lookup"><span data-stu-id="0f4d3-127">If not specified, the policy will be updated in the currently active api revision.</span></span>

```yaml
Type: System.String
Parameter Sets: SetApiLevel, SetOperationLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f4d3-128">-Context</span><span class="sxs-lookup"><span data-stu-id="0f4d3-128">-Context</span></span>
<span data-ttu-id="0f4d3-129">Указывает экземпляр **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="0f4d3-129">Specifies the instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="0f4d3-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f4d3-130">-DefaultProfile</span></span>
<span data-ttu-id="0f4d3-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0f4d3-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f4d3-132">-Format</span><span class="sxs-lookup"><span data-stu-id="0f4d3-132">-Format</span></span>
<span data-ttu-id="0f4d3-133">Задает формат политики.</span><span class="sxs-lookup"><span data-stu-id="0f4d3-133">Specifies the format of the policy.</span></span> <span data-ttu-id="0f4d3-134">При использовании `application/vnd.ms-azure-apim.policy+xml` выражения, содержащиеся в политике, должны быть преобразованы в XML-код.</span><span class="sxs-lookup"><span data-stu-id="0f4d3-134">When using `application/vnd.ms-azure-apim.policy+xml`, expressions contained within the policy must be XML-escaped.</span></span> <span data-ttu-id="0f4d3-135">При использовании `application/vnd.ms-azure-apim.policy.raw+xml` этого параметра **не** обязательно, чтобы политика была преобразована в XML-код.</span><span class="sxs-lookup"><span data-stu-id="0f4d3-135">When using `application/vnd.ms-azure-apim.policy.raw+xml` it is **not** necessary for the policy to be XML-escaped.</span></span>
<span data-ttu-id="0f4d3-136">Значение по умолчанию — `application/vnd.ms-azure-apim.policy+xml` .</span><span class="sxs-lookup"><span data-stu-id="0f4d3-136">The default value is `application/vnd.ms-azure-apim.policy+xml`.</span></span>
<span data-ttu-id="0f4d3-137">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="0f4d3-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="0f4d3-138">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="0f4d3-138">-OperationId</span></span>
<span data-ttu-id="0f4d3-139">Указывает идентификатор существующей операции.</span><span class="sxs-lookup"><span data-stu-id="0f4d3-139">Specifies the identifier of the existing operation.</span></span>
<span data-ttu-id="0f4d3-140">Если параметр задан с помощью ApiId, будет задана политика области действия.</span><span class="sxs-lookup"><span data-stu-id="0f4d3-140">If specified with ApiId will set operation-scope policy.</span></span>
<span data-ttu-id="0f4d3-141">Эти параметры являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="0f4d3-141">This parameters is required.</span></span>

```yaml
Type: System.String
Parameter Sets: SetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f4d3-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f4d3-142">-PassThru</span></span>
<span data-ttu-id="0f4d3-143">PassThru</span><span class="sxs-lookup"><span data-stu-id="0f4d3-143">passthru</span></span>

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

### <span data-ttu-id="0f4d3-144">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="0f4d3-144">-Policy</span></span>
<span data-ttu-id="0f4d3-145">Определяет документ политики в виде строки.</span><span class="sxs-lookup"><span data-stu-id="0f4d3-145">Specifies the policy document as a string.</span></span>
<span data-ttu-id="0f4d3-146">Этот параметр является обязательным, если не указан параметр- *PolicyFilePath* .</span><span class="sxs-lookup"><span data-stu-id="0f4d3-146">This parameter is required if the - *PolicyFilePath* is not specified.</span></span>

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

### <span data-ttu-id="0f4d3-147">-PolicyFilePath</span><span class="sxs-lookup"><span data-stu-id="0f4d3-147">-PolicyFilePath</span></span>
<span data-ttu-id="0f4d3-148">Задает путь к файлу политики.</span><span class="sxs-lookup"><span data-stu-id="0f4d3-148">Specifies the policy document file path.</span></span>
<span data-ttu-id="0f4d3-149">Этот параметр является обязательным, если параметр *политики* не указан.</span><span class="sxs-lookup"><span data-stu-id="0f4d3-149">This parameter is required if the *Policy* parameter is not specified.</span></span>

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

### <span data-ttu-id="0f4d3-150">-PolicyUrl</span><span class="sxs-lookup"><span data-stu-id="0f4d3-150">-PolicyUrl</span></span>
<span data-ttu-id="0f4d3-151">URL-адрес, на котором размещен документ политики.</span><span class="sxs-lookup"><span data-stu-id="0f4d3-151">The Url where the Policy document is hosted.</span></span> <span data-ttu-id="0f4d3-152">Этот параметр является обязательным, если не указан параметр-Policy или-PolicyFilePath.</span><span class="sxs-lookup"><span data-stu-id="0f4d3-152">This parameter is required if -Policy or -PolicyFilePath is not specified.</span></span>

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

### <span data-ttu-id="0f4d3-153">-ProductId</span><span class="sxs-lookup"><span data-stu-id="0f4d3-153">-ProductId</span></span>
<span data-ttu-id="0f4d3-154">Указывает идентификатор существующего продукта.</span><span class="sxs-lookup"><span data-stu-id="0f4d3-154">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="0f4d3-155">Если указан этот параметр, командлет задает политику области продукта.</span><span class="sxs-lookup"><span data-stu-id="0f4d3-155">If this parameter is specified, the cmdlet sets the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: SetProductLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f4d3-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f4d3-156">CommonParameters</span></span>
<span data-ttu-id="0f4d3-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0f4d3-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f4d3-158">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f4d3-158">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f4d3-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0f4d3-159">INPUTS</span></span>

### <span data-ttu-id="0f4d3-160">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0f4d3-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0f4d3-161">System. String</span><span class="sxs-lookup"><span data-stu-id="0f4d3-161">System.String</span></span>

### <span data-ttu-id="0f4d3-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0f4d3-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0f4d3-163">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f4d3-163">OUTPUTS</span></span>

### <span data-ttu-id="0f4d3-164">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0f4d3-164">System.Boolean</span></span>

## <span data-ttu-id="0f4d3-165">Пуск</span><span class="sxs-lookup"><span data-stu-id="0f4d3-165">NOTES</span></span>

## <span data-ttu-id="0f4d3-166">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0f4d3-166">RELATED LINKS</span></span>

[<span data-ttu-id="0f4d3-167">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0f4d3-167">Get-AzApiManagementPolicy</span></span>](./Get-AzApiManagementPolicy.md)

[<span data-ttu-id="0f4d3-168">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0f4d3-168">Remove-AzApiManagementPolicy</span></span>](./Remove-AzApiManagementPolicy.md)


