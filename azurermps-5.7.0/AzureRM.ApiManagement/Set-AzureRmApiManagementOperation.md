---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 67EE6EFB-3297-4D21-A6EC-B03F5FE82F84
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
ms.openlocfilehash: 4800d7d56d03071b57d25cdacfcf271defa9276f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565028"
---
# <span data-ttu-id="ebd2c-101">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="ebd2c-101">Set-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="ebd2c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ebd2c-102">SYNOPSIS</span></span>
<span data-ttu-id="ebd2c-103">Задает сведения об операции API.</span><span class="sxs-lookup"><span data-stu-id="ebd2c-103">Sets API operation details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ebd2c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ebd2c-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ebd2c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebd2c-105">DESCRIPTION</span></span>
<span data-ttu-id="ebd2c-106">Командлет **Set-AzureRmApiManagementOperation** задает сведения об операциях API.</span><span class="sxs-lookup"><span data-stu-id="ebd2c-106">The **Set-AzureRmApiManagementOperation** cmdlet sets API operation details.</span></span>

## <span data-ttu-id="ebd2c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ebd2c-107">EXAMPLES</span></span>

### <span data-ttu-id="ebd2c-108">Пример 1: Настройка сведений об операции</span><span class="sxs-lookup"><span data-stu-id="ebd2c-108">Example 1: Set the operation details</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIID -OperationId $OperationId -Name "Get Resource" -Method GET -UrlTemplate "/newresource" -Description "Use this operation to get newresource"
```

<span data-ttu-id="ebd2c-109">Эта команда задает сведения об операциях для управления API.</span><span class="sxs-lookup"><span data-stu-id="ebd2c-109">This command sets the operation details for API management.</span></span>

## <span data-ttu-id="ebd2c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ebd2c-110">PARAMETERS</span></span>

### <span data-ttu-id="ebd2c-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="ebd2c-111">-ApiId</span></span>
<span data-ttu-id="ebd2c-112">Указывает идентификатор API.</span><span class="sxs-lookup"><span data-stu-id="ebd2c-112">Specifies the identifier of the API.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebd2c-113">-Context</span><span class="sxs-lookup"><span data-stu-id="ebd2c-113">-Context</span></span>
<span data-ttu-id="ebd2c-114">Указывает экземпляр **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="ebd2c-114">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="ebd2c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebd2c-115">-DefaultProfile</span></span>
<span data-ttu-id="ebd2c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ebd2c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="ebd2c-117">-Описание</span><span class="sxs-lookup"><span data-stu-id="ebd2c-117">-Description</span></span>
<span data-ttu-id="ebd2c-118">Задает описание новой операции.</span><span class="sxs-lookup"><span data-stu-id="ebd2c-118">Specifies the description of the new operation.</span></span>

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

### <span data-ttu-id="ebd2c-119">-Method</span><span class="sxs-lookup"><span data-stu-id="ebd2c-119">-Method</span></span>
<span data-ttu-id="ebd2c-120">Задает метод HTTP для новой операции.</span><span class="sxs-lookup"><span data-stu-id="ebd2c-120">Specifies the HTTP method of the new operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebd2c-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ebd2c-121">-Name</span></span>
<span data-ttu-id="ebd2c-122">Указывает отображаемое имя для новой операции.</span><span class="sxs-lookup"><span data-stu-id="ebd2c-122">Specifies the display name of the new operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebd2c-123">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="ebd2c-123">-OperationId</span></span>
<span data-ttu-id="ebd2c-124">Указывает идентификатор существующей операции.</span><span class="sxs-lookup"><span data-stu-id="ebd2c-124">Specifies the identifier of the existing operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebd2c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ebd2c-125">-PassThru</span></span>
<span data-ttu-id="ebd2c-126">PassThru</span><span class="sxs-lookup"><span data-stu-id="ebd2c-126">passthru</span></span>

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

### <span data-ttu-id="ebd2c-127">-Request</span><span class="sxs-lookup"><span data-stu-id="ebd2c-127">-Request</span></span>
<span data-ttu-id="ebd2c-128">Задает сведения о запросе операции.</span><span class="sxs-lookup"><span data-stu-id="ebd2c-128">Specifies the operation request details.</span></span>

```yaml
Type: PsApiManagementRequest
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebd2c-129">-Ответы</span><span class="sxs-lookup"><span data-stu-id="ebd2c-129">-Responses</span></span>
<span data-ttu-id="ebd2c-130">Указывает массив возможных ответов операций.</span><span class="sxs-lookup"><span data-stu-id="ebd2c-130">Specifies an array of possible operation responses.</span></span>

```yaml
Type: PsApiManagementResponse[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebd2c-131">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="ebd2c-131">-TemplateParameters</span></span>
<span data-ttu-id="ebd2c-132">Задает массив или параметры, определенные в параметре *UrlTemplate*.</span><span class="sxs-lookup"><span data-stu-id="ebd2c-132">Specifies an array or parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="ebd2c-133">Если значение не задано, на основе UrlTemplate будет создано значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ebd2c-133">If you do not specify a value, a default value will be generated based on the UrlTemplate.</span></span>
<span data-ttu-id="ebd2c-134">С помощью этого параметра можно получить дополнительные сведения о таких параметрах, как описание, тип и другие возможные значения.</span><span class="sxs-lookup"><span data-stu-id="ebd2c-134">Use the parameter to give more details on parameters such as description, type, and other possible values.</span></span>

```yaml
Type: PsApiManagementParameter[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebd2c-135">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="ebd2c-135">-UrlTemplate</span></span>
<span data-ttu-id="ebd2c-136">Задает шаблон URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="ebd2c-136">Specifies the URL template.</span></span>
<span data-ttu-id="ebd2c-137">Например: Customers/{CID}/заказы/{OID}/? Дата = {Date}.</span><span class="sxs-lookup"><span data-stu-id="ebd2c-137">For instance: customers/{cid}/orders/{oid}/?date={date}.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebd2c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebd2c-138">CommonParameters</span></span>
<span data-ttu-id="ebd2c-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ebd2c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebd2c-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebd2c-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebd2c-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ebd2c-141">INPUTS</span></span>

### <span data-ttu-id="ebd2c-142">Ничего</span><span class="sxs-lookup"><span data-stu-id="ebd2c-142">None</span></span>
<span data-ttu-id="ebd2c-143">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="ebd2c-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ebd2c-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebd2c-144">OUTPUTS</span></span>

### <span data-ttu-id="ebd2c-145">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="ebd2c-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="ebd2c-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="ebd2c-146">NOTES</span></span>

## <span data-ttu-id="ebd2c-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ebd2c-147">RELATED LINKS</span></span>

[<span data-ttu-id="ebd2c-148">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="ebd2c-148">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="ebd2c-149">New-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="ebd2c-149">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="ebd2c-150">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="ebd2c-150">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)


