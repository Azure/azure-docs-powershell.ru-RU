---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 0f9ee1c2190dbc3d657ecc52cd85b6af8b0cac4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732660"
---
# <span data-ttu-id="6da1f-101">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6da1f-101">Set-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="6da1f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6da1f-102">SYNOPSIS</span></span>
<span data-ttu-id="6da1f-103">Задает указанную политику области для управления API.</span><span class="sxs-lookup"><span data-stu-id="6da1f-103">Sets the specified scope policy for API Management.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6da1f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6da1f-104">SYNTAX</span></span>

### <span data-ttu-id="6da1f-105">SetTenantLevel (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6da1f-105">SetTenantLevel (Default)</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6da1f-106">SetProductLevel</span><span class="sxs-lookup"><span data-stu-id="6da1f-106">SetProductLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6da1f-107">SetApiLevel</span><span class="sxs-lookup"><span data-stu-id="6da1f-107">SetApiLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6da1f-108">SetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="6da1f-108">SetOperationLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6da1f-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6da1f-109">DESCRIPTION</span></span>
<span data-ttu-id="6da1f-110">Командлет **Set-AzureRmApiManagementPolicy** задает указанную политику области для управления API.</span><span class="sxs-lookup"><span data-stu-id="6da1f-110">The **Set-AzureRmApiManagementPolicy** cmdlet sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="6da1f-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6da1f-111">EXAMPLES</span></span>

### <span data-ttu-id="6da1f-112">Пример 1: Настройка политики уровня клиента</span><span class="sxs-lookup"><span data-stu-id="6da1f-112">Example 1: Set the tenant level policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="6da1f-113">Эта команда задает политику уровня клиента из файла с именем tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="6da1f-113">This command sets the tenant level policy from a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="6da1f-114">Пример 2: Настройка политики для области продукта</span><span class="sxs-lookup"><span data-stu-id="6da1f-114">Example 2: Set a product-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -ProductId "0123456789" -Policy $PolicyString
```

<span data-ttu-id="6da1f-115">Эта команда задает политику области продукта для управления API.</span><span class="sxs-lookup"><span data-stu-id="6da1f-115">This command sets the product-scope policy for API Management.</span></span>

### <span data-ttu-id="6da1f-116">Пример 3: Настройка политики области API</span><span class="sxs-lookup"><span data-stu-id="6da1f-116">Example 3: Set API-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -Policy $PolicyString
```

<span data-ttu-id="6da1f-117">Эта команда задает политику области API для управления API.</span><span class="sxs-lookup"><span data-stu-id="6da1f-117">This command sets API-scope policy for API Management.</span></span>

### <span data-ttu-id="6da1f-118">Пример 4: Настройка политики области действия</span><span class="sxs-lookup"><span data-stu-id="6da1f-118">Example 4: Set operation-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

<span data-ttu-id="6da1f-119">Эта команда задает политику области действия для управления API.</span><span class="sxs-lookup"><span data-stu-id="6da1f-119">This command sets operation-scope policy for API Management.</span></span>

## <span data-ttu-id="6da1f-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6da1f-120">PARAMETERS</span></span>

### <span data-ttu-id="6da1f-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="6da1f-121">-ApiId</span></span>
<span data-ttu-id="6da1f-122">Указывает идентификатор существующего API.</span><span class="sxs-lookup"><span data-stu-id="6da1f-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="6da1f-123">Если указать этот параметр, командлет задает политику области API.</span><span class="sxs-lookup"><span data-stu-id="6da1f-123">If you specify this parameter, the cmdlet sets the API-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: SetApiLevel, SetOperationLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6da1f-124">-Context</span><span class="sxs-lookup"><span data-stu-id="6da1f-124">-Context</span></span>
<span data-ttu-id="6da1f-125">Указывает экземпляр **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="6da1f-125">Specifies the instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="6da1f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6da1f-126">-DefaultProfile</span></span>
<span data-ttu-id="6da1f-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6da1f-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="6da1f-128">-Format</span><span class="sxs-lookup"><span data-stu-id="6da1f-128">-Format</span></span>
<span data-ttu-id="6da1f-129">Задает формат политики.</span><span class="sxs-lookup"><span data-stu-id="6da1f-129">Specifies the format of the policy.</span></span>
<span data-ttu-id="6da1f-130">Значением по умолчанию является "application/vnd. MS-Azure-apim. Policy + XML".</span><span class="sxs-lookup"><span data-stu-id="6da1f-130">The default value is "application/vnd.ms-azure-apim.policy+xml".</span></span>

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

### <span data-ttu-id="6da1f-131">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="6da1f-131">-OperationId</span></span>
<span data-ttu-id="6da1f-132">Указывает идентификатор существующей операции.</span><span class="sxs-lookup"><span data-stu-id="6da1f-132">Specifies the identifier of the existing operation.</span></span>
<span data-ttu-id="6da1f-133">Если параметр задан с помощью ApiId, будет задана политика области действия.</span><span class="sxs-lookup"><span data-stu-id="6da1f-133">If specified with ApiId will set operation-scope policy.</span></span>
<span data-ttu-id="6da1f-134">Эти параметры являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="6da1f-134">This parameters is required.</span></span>

```yaml
Type: String
Parameter Sets: SetOperationLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6da1f-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6da1f-135">-PassThru</span></span>
<span data-ttu-id="6da1f-136">PassThru</span><span class="sxs-lookup"><span data-stu-id="6da1f-136">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6da1f-137">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="6da1f-137">-Policy</span></span>
<span data-ttu-id="6da1f-138">Определяет документ политики в виде строки.</span><span class="sxs-lookup"><span data-stu-id="6da1f-138">Specifies the policy document as a string.</span></span>
<span data-ttu-id="6da1f-139">Этот параметр является обязательным, если не указан параметр- *PolicyFilePath* .</span><span class="sxs-lookup"><span data-stu-id="6da1f-139">This parameter is required if the - *PolicyFilePath* is not specified.</span></span>

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

### <span data-ttu-id="6da1f-140">-PolicyFilePath</span><span class="sxs-lookup"><span data-stu-id="6da1f-140">-PolicyFilePath</span></span>
<span data-ttu-id="6da1f-141">Задает путь к файлу политики.</span><span class="sxs-lookup"><span data-stu-id="6da1f-141">Specifies the policy document file path.</span></span>
<span data-ttu-id="6da1f-142">Этот параметр является обязательным, если параметр *политики* не указан.</span><span class="sxs-lookup"><span data-stu-id="6da1f-142">This parameter is required if the *Policy* parameter is not specified.</span></span>

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

### <span data-ttu-id="6da1f-143">-ProductId</span><span class="sxs-lookup"><span data-stu-id="6da1f-143">-ProductId</span></span>
<span data-ttu-id="6da1f-144">Указывает идентификатор существующего продукта.</span><span class="sxs-lookup"><span data-stu-id="6da1f-144">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="6da1f-145">Если указан этот параметр, командлет задает политику области продукта.</span><span class="sxs-lookup"><span data-stu-id="6da1f-145">If this parameter is specified, the cmdlet sets the product-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: SetProductLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6da1f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6da1f-146">CommonParameters</span></span>
<span data-ttu-id="6da1f-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6da1f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6da1f-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6da1f-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6da1f-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6da1f-149">INPUTS</span></span>

### <span data-ttu-id="6da1f-150">Ничего</span><span class="sxs-lookup"><span data-stu-id="6da1f-150">None</span></span>
<span data-ttu-id="6da1f-151">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="6da1f-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6da1f-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6da1f-152">OUTPUTS</span></span>

### <span data-ttu-id="6da1f-153">логических</span><span class="sxs-lookup"><span data-stu-id="6da1f-153">bool</span></span>

## <span data-ttu-id="6da1f-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="6da1f-154">NOTES</span></span>

## <span data-ttu-id="6da1f-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6da1f-155">RELATED LINKS</span></span>

[<span data-ttu-id="6da1f-156">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6da1f-156">Get-AzureRmApiManagementPolicy</span></span>](./Get-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="6da1f-157">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6da1f-157">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)


