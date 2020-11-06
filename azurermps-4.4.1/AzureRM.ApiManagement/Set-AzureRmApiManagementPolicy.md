---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 8073df3946f5bf42ee8b0e5f2c7ae7881e905eaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565713"
---
# <span data-ttu-id="73711-101">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="73711-101">Set-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="73711-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="73711-102">SYNOPSIS</span></span>
<span data-ttu-id="73711-103">Задает указанную политику области для управления API.</span><span class="sxs-lookup"><span data-stu-id="73711-103">Sets the specified scope policy for API Management.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73711-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="73711-104">SYNTAX</span></span>

### <span data-ttu-id="73711-105">Уровень клиента (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="73711-105">Tenant level (Default)</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73711-106">Уровень продукта</span><span class="sxs-lookup"><span data-stu-id="73711-106">Product level</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="73711-107">Уровень API</span><span class="sxs-lookup"><span data-stu-id="73711-107">API level</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="73711-108">Уровень операций</span><span class="sxs-lookup"><span data-stu-id="73711-108">Operation level</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73711-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="73711-109">DESCRIPTION</span></span>
<span data-ttu-id="73711-110">Командлет **Set-AzureRmApiManagementPolicy** задает указанную политику области для управления API.</span><span class="sxs-lookup"><span data-stu-id="73711-110">The **Set-AzureRmApiManagementPolicy** cmdlet sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="73711-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="73711-111">EXAMPLES</span></span>

### <span data-ttu-id="73711-112">Пример 1: Настройка политики уровня клиента</span><span class="sxs-lookup"><span data-stu-id="73711-112">Example 1: Set the tenant level policy</span></span>
```
PS C:\>Set-AzureRmApiManagementPolicy -Context $APImContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="73711-113">Эта команда задает политику уровня клиента из файла с именем tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="73711-113">This command sets the tenant level policy from a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="73711-114">Пример 2: Настройка политики для области продукта</span><span class="sxs-lookup"><span data-stu-id="73711-114">Example 2: Set a product-scope policy</span></span>
```
PS C:\>Set-AzureRmApiManagementPolicy -Context $APImContext -ProductId "0123456789" -Policy $PolicyString
```

<span data-ttu-id="73711-115">Эта команда задает политику области продукта для управления API.</span><span class="sxs-lookup"><span data-stu-id="73711-115">This command sets the product-scope policy for API Management.</span></span>

### <span data-ttu-id="73711-116">Пример 3: Настройка политики области API</span><span class="sxs-lookup"><span data-stu-id="73711-116">Example 3: Set API-scope policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210" -Policy $PolicyString
```

<span data-ttu-id="73711-117">Эта команда задает политику области API для управления API.</span><span class="sxs-lookup"><span data-stu-id="73711-117">This command sets API-scope policy for API Management.</span></span>

### <span data-ttu-id="73711-118">Пример 4: Настройка политики области действия</span><span class="sxs-lookup"><span data-stu-id="73711-118">Example 4: Set operation-scope policy</span></span>
```
PS C:\>Set-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

<span data-ttu-id="73711-119">Эта команда задает политику области действия для управления API.</span><span class="sxs-lookup"><span data-stu-id="73711-119">This command sets operation-scope policy for API Management.</span></span>

## <span data-ttu-id="73711-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="73711-120">PARAMETERS</span></span>

### <span data-ttu-id="73711-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="73711-121">-ApiId</span></span>
<span data-ttu-id="73711-122">Указывает идентификатор существующего API.</span><span class="sxs-lookup"><span data-stu-id="73711-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="73711-123">Если указать этот параметр, командлет задает политику области API.</span><span class="sxs-lookup"><span data-stu-id="73711-123">If you specify this parameter, the cmdlet sets the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: API level, Operation level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73711-124">-Context</span><span class="sxs-lookup"><span data-stu-id="73711-124">-Context</span></span>
<span data-ttu-id="73711-125">Указывает экземпляр **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="73711-125">Specifies the instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="73711-126">-Format</span><span class="sxs-lookup"><span data-stu-id="73711-126">-Format</span></span>
<span data-ttu-id="73711-127">Задает формат политики.</span><span class="sxs-lookup"><span data-stu-id="73711-127">Specifies the format of the policy.</span></span>
<span data-ttu-id="73711-128">Значением по умолчанию является "application/vnd. MS-Azure-apim. Policy + XML".</span><span class="sxs-lookup"><span data-stu-id="73711-128">The default value is "application/vnd.ms-azure-apim.policy+xml".</span></span>

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

### <span data-ttu-id="73711-129">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="73711-129">-OperationId</span></span>
<span data-ttu-id="73711-130">Указывает идентификатор существующей операции.</span><span class="sxs-lookup"><span data-stu-id="73711-130">Specifies the identifier of the existing operation.</span></span>
<span data-ttu-id="73711-131">Если параметр задан с помощью ApiId, будет задана политика области действия.</span><span class="sxs-lookup"><span data-stu-id="73711-131">If specified with ApiId will set operation-scope policy.</span></span>
<span data-ttu-id="73711-132">Эти параметры являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="73711-132">This parameters is required.</span></span>

```yaml
Type: System.String
Parameter Sets: Operation level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73711-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="73711-133">-PassThru</span></span>
<span data-ttu-id="73711-134">PassThru</span><span class="sxs-lookup"><span data-stu-id="73711-134">passthru</span></span>

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

### <span data-ttu-id="73711-135">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="73711-135">-Policy</span></span>
<span data-ttu-id="73711-136">Определяет документ политики в виде строки.</span><span class="sxs-lookup"><span data-stu-id="73711-136">Specifies the policy document as a string.</span></span>
<span data-ttu-id="73711-137">Этот параметр является обязательным, если не указан параметр- *PolicyFilePath* .</span><span class="sxs-lookup"><span data-stu-id="73711-137">This parameter is required if the - *PolicyFilePath* is not specified.</span></span>

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

### <span data-ttu-id="73711-138">-PolicyFilePath</span><span class="sxs-lookup"><span data-stu-id="73711-138">-PolicyFilePath</span></span>
<span data-ttu-id="73711-139">Задает путь к файлу политики.</span><span class="sxs-lookup"><span data-stu-id="73711-139">Specifies the policy document file path.</span></span>
<span data-ttu-id="73711-140">Этот параметр является обязательным, если параметр *политики* не указан.</span><span class="sxs-lookup"><span data-stu-id="73711-140">This parameter is required if the *Policy* parameter is not specified.</span></span>

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

### <span data-ttu-id="73711-141">-ProductId</span><span class="sxs-lookup"><span data-stu-id="73711-141">-ProductId</span></span>
<span data-ttu-id="73711-142">Указывает идентификатор существующего продукта.</span><span class="sxs-lookup"><span data-stu-id="73711-142">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="73711-143">Если указан этот параметр, командлет задает политику области продукта.</span><span class="sxs-lookup"><span data-stu-id="73711-143">If this parameter is specified, the cmdlet sets the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: Product level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73711-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73711-144">-DefaultProfile</span></span>
<span data-ttu-id="73711-145">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="73711-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73711-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73711-146">CommonParameters</span></span>
<span data-ttu-id="73711-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="73711-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73711-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73711-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73711-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="73711-149">INPUTS</span></span>

## <span data-ttu-id="73711-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="73711-150">OUTPUTS</span></span>

### <span data-ttu-id="73711-151">логических</span><span class="sxs-lookup"><span data-stu-id="73711-151">bool</span></span>

## <span data-ttu-id="73711-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="73711-152">NOTES</span></span>

## <span data-ttu-id="73711-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="73711-153">RELATED LINKS</span></span>

[<span data-ttu-id="73711-154">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="73711-154">Get-AzureRmApiManagementPolicy</span></span>](./Get-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="73711-155">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="73711-155">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)


