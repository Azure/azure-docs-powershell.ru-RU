---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 75bb963195244a5a1a27ca004eb2795b6b5bb556
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558620"
---
# <span data-ttu-id="dec17-101">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="dec17-101">Set-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="dec17-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dec17-102">SYNOPSIS</span></span>
<span data-ttu-id="dec17-103">Задает указанную политику области для управления API.</span><span class="sxs-lookup"><span data-stu-id="dec17-103">Sets the specified scope policy for API Management.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dec17-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dec17-104">SYNTAX</span></span>

### <span data-ttu-id="dec17-105">SetTenantLevel (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dec17-105">SetTenantLevel (Default)</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dec17-106">SetProductLevel</span><span class="sxs-lookup"><span data-stu-id="dec17-106">SetProductLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dec17-107">SetApiLevel</span><span class="sxs-lookup"><span data-stu-id="dec17-107">SetApiLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dec17-108">SetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="dec17-108">SetOperationLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>]
 [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dec17-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dec17-109">DESCRIPTION</span></span>
<span data-ttu-id="dec17-110">Командлет **Set-AzureRmApiManagementPolicy** задает указанную политику области для управления API.</span><span class="sxs-lookup"><span data-stu-id="dec17-110">The **Set-AzureRmApiManagementPolicy** cmdlet sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="dec17-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dec17-111">EXAMPLES</span></span>

### <span data-ttu-id="dec17-112">Пример 1: Настройка политики уровня клиента</span><span class="sxs-lookup"><span data-stu-id="dec17-112">Example 1: Set the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="dec17-113">Эта команда задает политику уровня клиента из файла с именем tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="dec17-113">This command sets the tenant level policy from a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="dec17-114">Пример 2: Настройка политики для области продукта</span><span class="sxs-lookup"><span data-stu-id="dec17-114">Example 2: Set a product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -ProductId "0123456789" -Policy $PolicyString
```

<span data-ttu-id="dec17-115">Эта команда задает политику области продукта для управления API.</span><span class="sxs-lookup"><span data-stu-id="dec17-115">This command sets the product-scope policy for API Management.</span></span>

### <span data-ttu-id="dec17-116">Пример 3: Настройка политики области API</span><span class="sxs-lookup"><span data-stu-id="dec17-116">Example 3: Set API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -Policy $PolicyString
```

<span data-ttu-id="dec17-117">Эта команда задает политику области API для управления API.</span><span class="sxs-lookup"><span data-stu-id="dec17-117">This command sets API-scope policy for API Management.</span></span>

### <span data-ttu-id="dec17-118">Пример 4: Настройка политики области действия</span><span class="sxs-lookup"><span data-stu-id="dec17-118">Example 4: Set operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

<span data-ttu-id="dec17-119">Эта команда задает политику области действия для управления API.</span><span class="sxs-lookup"><span data-stu-id="dec17-119">This command sets operation-scope policy for API Management.</span></span>

## <span data-ttu-id="dec17-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dec17-120">PARAMETERS</span></span>

### <span data-ttu-id="dec17-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="dec17-121">-ApiId</span></span>
<span data-ttu-id="dec17-122">Указывает идентификатор существующего API.</span><span class="sxs-lookup"><span data-stu-id="dec17-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="dec17-123">Если указать этот параметр, командлет задает политику области API.</span><span class="sxs-lookup"><span data-stu-id="dec17-123">If you specify this parameter, the cmdlet sets the API-scope policy.</span></span>

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

### <span data-ttu-id="dec17-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="dec17-124">-ApiRevision</span></span>
<span data-ttu-id="dec17-125">Идентификатор редакции API.</span><span class="sxs-lookup"><span data-stu-id="dec17-125">Identifier of API Revision.</span></span> <span data-ttu-id="dec17-126">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="dec17-126">This parameter is optional.</span></span> <span data-ttu-id="dec17-127">Если не указано, политика будет обновляться в текущей версии API.</span><span class="sxs-lookup"><span data-stu-id="dec17-127">If not specified, the policy will be updated in the currently active api revision.</span></span>

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

### <span data-ttu-id="dec17-128">-Context</span><span class="sxs-lookup"><span data-stu-id="dec17-128">-Context</span></span>
<span data-ttu-id="dec17-129">Указывает экземпляр **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="dec17-129">Specifies the instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="dec17-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dec17-130">-DefaultProfile</span></span>
<span data-ttu-id="dec17-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dec17-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dec17-132">-Format</span><span class="sxs-lookup"><span data-stu-id="dec17-132">-Format</span></span>
<span data-ttu-id="dec17-133">Задает формат политики.</span><span class="sxs-lookup"><span data-stu-id="dec17-133">Specifies the format of the policy.</span></span> <span data-ttu-id="dec17-134">При использовании `application/vnd.ms-azure-apim.policy+xml` выражения, содержащиеся в политике, должны быть преобразованы в XML-код.</span><span class="sxs-lookup"><span data-stu-id="dec17-134">When using `application/vnd.ms-azure-apim.policy+xml`, expressions contained within the policy must be XML-escaped.</span></span> <span data-ttu-id="dec17-135">При использовании `application/vnd.ms-azure-apim.policy.raw+xml` этого параметра **не** обязательно, чтобы политика была преобразована в XML-код.</span><span class="sxs-lookup"><span data-stu-id="dec17-135">When using `application/vnd.ms-azure-apim.policy.raw+xml` it is **not** necessary for the policy to be XML-escaped.</span></span>
<span data-ttu-id="dec17-136">Значение по умолчанию — `application/vnd.ms-azure-apim.policy+xml` .</span><span class="sxs-lookup"><span data-stu-id="dec17-136">The default value is `application/vnd.ms-azure-apim.policy+xml`.</span></span>
<span data-ttu-id="dec17-137">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="dec17-137">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: application/vnd.ms-azure-apim.policy.raw+xml, application/vnd.ms-azure-apim.policy+xml

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dec17-138">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="dec17-138">-OperationId</span></span>
<span data-ttu-id="dec17-139">Указывает идентификатор существующей операции.</span><span class="sxs-lookup"><span data-stu-id="dec17-139">Specifies the identifier of the existing operation.</span></span>
<span data-ttu-id="dec17-140">Если параметр задан с помощью ApiId, будет задана политика области действия.</span><span class="sxs-lookup"><span data-stu-id="dec17-140">If specified with ApiId will set operation-scope policy.</span></span>
<span data-ttu-id="dec17-141">Эти параметры являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="dec17-141">This parameters is required.</span></span>

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

### <span data-ttu-id="dec17-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dec17-142">-PassThru</span></span>
<span data-ttu-id="dec17-143">PassThru</span><span class="sxs-lookup"><span data-stu-id="dec17-143">passthru</span></span>

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

### <span data-ttu-id="dec17-144">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="dec17-144">-Policy</span></span>
<span data-ttu-id="dec17-145">Определяет документ политики в виде строки.</span><span class="sxs-lookup"><span data-stu-id="dec17-145">Specifies the policy document as a string.</span></span>
<span data-ttu-id="dec17-146">Этот параметр является обязательным, если не указан параметр- *PolicyFilePath* .</span><span class="sxs-lookup"><span data-stu-id="dec17-146">This parameter is required if the - *PolicyFilePath* is not specified.</span></span>

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

### <span data-ttu-id="dec17-147">-PolicyFilePath</span><span class="sxs-lookup"><span data-stu-id="dec17-147">-PolicyFilePath</span></span>
<span data-ttu-id="dec17-148">Задает путь к файлу политики.</span><span class="sxs-lookup"><span data-stu-id="dec17-148">Specifies the policy document file path.</span></span>
<span data-ttu-id="dec17-149">Этот параметр является обязательным, если параметр *политики* не указан.</span><span class="sxs-lookup"><span data-stu-id="dec17-149">This parameter is required if the *Policy* parameter is not specified.</span></span>

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

### <span data-ttu-id="dec17-150">-PolicyUrl</span><span class="sxs-lookup"><span data-stu-id="dec17-150">-PolicyUrl</span></span>
<span data-ttu-id="dec17-151">URL-адрес, на котором размещен документ политики.</span><span class="sxs-lookup"><span data-stu-id="dec17-151">The Url where the Policy document is hosted.</span></span> <span data-ttu-id="dec17-152">Этот параметр является обязательным, если не указан параметр-Policy или-PolicyFilePath.</span><span class="sxs-lookup"><span data-stu-id="dec17-152">This parameter is required if -Policy or -PolicyFilePath is not specified.</span></span>

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

### <span data-ttu-id="dec17-153">-ProductId</span><span class="sxs-lookup"><span data-stu-id="dec17-153">-ProductId</span></span>
<span data-ttu-id="dec17-154">Указывает идентификатор существующего продукта.</span><span class="sxs-lookup"><span data-stu-id="dec17-154">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="dec17-155">Если указан этот параметр, командлет задает политику области продукта.</span><span class="sxs-lookup"><span data-stu-id="dec17-155">If this parameter is specified, the cmdlet sets the product-scope policy.</span></span>

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

### <span data-ttu-id="dec17-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dec17-156">CommonParameters</span></span>
<span data-ttu-id="dec17-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dec17-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dec17-158">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dec17-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dec17-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dec17-159">INPUTS</span></span>

### <span data-ttu-id="dec17-160">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="dec17-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="dec17-161">System. String</span><span class="sxs-lookup"><span data-stu-id="dec17-161">System.String</span></span>

### <span data-ttu-id="dec17-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="dec17-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="dec17-163">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dec17-163">OUTPUTS</span></span>

### <span data-ttu-id="dec17-164">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dec17-164">System.Boolean</span></span>

## <span data-ttu-id="dec17-165">Пуск</span><span class="sxs-lookup"><span data-stu-id="dec17-165">NOTES</span></span>

## <span data-ttu-id="dec17-166">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dec17-166">RELATED LINKS</span></span>

[<span data-ttu-id="dec17-167">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="dec17-167">Get-AzureRmApiManagementPolicy</span></span>](./Get-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="dec17-168">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="dec17-168">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)


