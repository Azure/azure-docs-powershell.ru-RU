---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 31b38d07aea51ad1e6bd097cc0c9f7f342e1bfb2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563803"
---
# <span data-ttu-id="0510d-101">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0510d-101">Get-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="0510d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0510d-102">SYNOPSIS</span></span>
<span data-ttu-id="0510d-103">Получает указанную политику области.</span><span class="sxs-lookup"><span data-stu-id="0510d-103">Gets the specified scope policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0510d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0510d-104">SYNTAX</span></span>

### <span data-ttu-id="0510d-105">GetTenantLevel (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0510d-105">GetTenantLevel (Default)</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0510d-106">GetProductLevel</span><span class="sxs-lookup"><span data-stu-id="0510d-106">GetProductLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0510d-107">GetApiLevel</span><span class="sxs-lookup"><span data-stu-id="0510d-107">GetApiLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0510d-108">GetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="0510d-108">GetOperationLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> -OperationId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0510d-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0510d-109">DESCRIPTION</span></span>
<span data-ttu-id="0510d-110">Командлет **Get-AzureRmApiManagementPolicy** получает указанную политику области.</span><span class="sxs-lookup"><span data-stu-id="0510d-110">The **Get-AzureRmApiManagementPolicy** cmdlet gets the specified scope policy.</span></span>

## <span data-ttu-id="0510d-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0510d-111">EXAMPLES</span></span>

### <span data-ttu-id="0510d-112">Пример 1: получение политики уровня клиента</span><span class="sxs-lookup"><span data-stu-id="0510d-112">Example 1: Get the tenant level policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="0510d-113">Эта команда получает политику уровня клиента и сохраняет ее в файле с именем tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="0510d-113">This command gets tenant level policy and saves it to a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="0510d-114">Пример 2: получение политики для области продукта</span><span class="sxs-lookup"><span data-stu-id="0510d-114">Example 2: Get the product-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="0510d-115">Эта команда получает политику области продукта</span><span class="sxs-lookup"><span data-stu-id="0510d-115">This command gets product-scope policy</span></span>

### <span data-ttu-id="0510d-116">Пример 3: получение политики области API</span><span class="sxs-lookup"><span data-stu-id="0510d-116">Example 3: Get the API-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="0510d-117">Эта команда получает политику области API.</span><span class="sxs-lookup"><span data-stu-id="0510d-117">This command gets API-scope policy.</span></span>

### <span data-ttu-id="0510d-118">Пример 4: получение политики области действия для операции</span><span class="sxs-lookup"><span data-stu-id="0510d-118">Example 4: Get the operation-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="0510d-119">Эта команда получает политику области действия.</span><span class="sxs-lookup"><span data-stu-id="0510d-119">This command gets the operation-scope policy.</span></span>

## <span data-ttu-id="0510d-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0510d-120">PARAMETERS</span></span>

### <span data-ttu-id="0510d-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="0510d-121">-ApiId</span></span>
<span data-ttu-id="0510d-122">Указывает идентификатор существующего API.</span><span class="sxs-lookup"><span data-stu-id="0510d-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="0510d-123">Если указать этот параметр, командлет возвращает политику области API.</span><span class="sxs-lookup"><span data-stu-id="0510d-123">If you specify this parameter the cmdlet returns the API-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0510d-124">-Context</span><span class="sxs-lookup"><span data-stu-id="0510d-124">-Context</span></span>
<span data-ttu-id="0510d-125">Указывает экземпляр **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="0510d-125">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="0510d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0510d-126">-DefaultProfile</span></span>
<span data-ttu-id="0510d-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0510d-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="0510d-128">-Force</span><span class="sxs-lookup"><span data-stu-id="0510d-128">-Force</span></span>
<span data-ttu-id="0510d-129">ps_force</span><span class="sxs-lookup"><span data-stu-id="0510d-129">ps_force</span></span>

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

### <span data-ttu-id="0510d-130">-Format</span><span class="sxs-lookup"><span data-stu-id="0510d-130">-Format</span></span>
<span data-ttu-id="0510d-131">Задает формат политики управления API.</span><span class="sxs-lookup"><span data-stu-id="0510d-131">Specifies the format of the API management policy.</span></span>
<span data-ttu-id="0510d-132">Значением по умолчанию для этого параметра является "application/vnd. MS-Azure-apim. Policy + XML".</span><span class="sxs-lookup"><span data-stu-id="0510d-132">The default value for this parameter is "application/vnd.ms-azure-apim.policy+xml".</span></span>

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

### <span data-ttu-id="0510d-133">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="0510d-133">-OperationId</span></span>
<span data-ttu-id="0510d-134">Указывает идентификатор существующей операции API.</span><span class="sxs-lookup"><span data-stu-id="0510d-134">Specifies the identifier of the existing API operation.</span></span>
<span data-ttu-id="0510d-135">Если указать этот параметр в *ApiId* , командлет возвращает политику области действия.</span><span class="sxs-lookup"><span data-stu-id="0510d-135">If you specify this parameter with *ApiId* the cmdlet returns operation-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: GetOperationLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0510d-136">-ProductId</span><span class="sxs-lookup"><span data-stu-id="0510d-136">-ProductId</span></span>
<span data-ttu-id="0510d-137">Указывает идентификатор существующего продукта.</span><span class="sxs-lookup"><span data-stu-id="0510d-137">Specifies the identifier of an existing product.</span></span>
<span data-ttu-id="0510d-138">Если указать этот параметр, командлет возвращает политику области продукта.</span><span class="sxs-lookup"><span data-stu-id="0510d-138">If you specify this parameter the cmdlet returns the product-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: GetProductLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0510d-139">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="0510d-139">-SaveAs</span></span>
<span data-ttu-id="0510d-140">Задает путь к файлу, в который нужно сохранить результат.</span><span class="sxs-lookup"><span data-stu-id="0510d-140">Specifies the file path to save the result to.</span></span>
<span data-ttu-id="0510d-141">Если этот параметр не указан, результат будет конвейерная, как Sting.</span><span class="sxs-lookup"><span data-stu-id="0510d-141">If you do not specify this parameter the result is pipelined as a sting.</span></span>

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

### <span data-ttu-id="0510d-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0510d-142">-Confirm</span></span>
<span data-ttu-id="0510d-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0510d-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0510d-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0510d-144">-WhatIf</span></span>
<span data-ttu-id="0510d-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0510d-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0510d-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0510d-146">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0510d-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0510d-147">CommonParameters</span></span>
<span data-ttu-id="0510d-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0510d-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0510d-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0510d-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0510d-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0510d-150">INPUTS</span></span>

### <span data-ttu-id="0510d-151">Ничего</span><span class="sxs-lookup"><span data-stu-id="0510d-151">None</span></span>
<span data-ttu-id="0510d-152">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="0510d-152">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0510d-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0510d-153">OUTPUTS</span></span>

### <span data-ttu-id="0510d-154">Подстрок</span><span class="sxs-lookup"><span data-stu-id="0510d-154">String</span></span>

## <span data-ttu-id="0510d-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="0510d-155">NOTES</span></span>

## <span data-ttu-id="0510d-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0510d-156">RELATED LINKS</span></span>

[<span data-ttu-id="0510d-157">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0510d-157">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="0510d-158">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0510d-158">Set-AzureRmApiManagementPolicy</span></span>](./Set-AzureRmApiManagementPolicy.md)


