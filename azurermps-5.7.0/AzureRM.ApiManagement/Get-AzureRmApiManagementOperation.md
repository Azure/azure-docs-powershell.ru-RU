---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
ms.openlocfilehash: 1b1547485a4758764cf02eaca4fd7bc26d4ef990
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567492"
---
# <span data-ttu-id="51430-101">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="51430-101">Get-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="51430-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="51430-102">SYNOPSIS</span></span>
<span data-ttu-id="51430-103">Возвращает список или указанную операцию API.</span><span class="sxs-lookup"><span data-stu-id="51430-103">Gets a list or a specified API Operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51430-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="51430-104">SYNTAX</span></span>

### <span data-ttu-id="51430-105">GetAllApiOperations (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="51430-105">GetAllApiOperations (Default)</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51430-106">GetById</span><span class="sxs-lookup"><span data-stu-id="51430-106">GetById</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51430-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="51430-107">DESCRIPTION</span></span>
<span data-ttu-id="51430-108">Функция **Get-AzureRmApiManagementOperation** возвращает список или указанную операцию API.</span><span class="sxs-lookup"><span data-stu-id="51430-108">The **Get-AzureRmApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="51430-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="51430-109">EXAMPLES</span></span>

### <span data-ttu-id="51430-110">Пример 1: получение всех операций управления API</span><span class="sxs-lookup"><span data-stu-id="51430-110">Example 1: Get all API management operations</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIId
```

<span data-ttu-id="51430-111">Эта команда получает все операции по управлению API.</span><span class="sxs-lookup"><span data-stu-id="51430-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="51430-112">Пример 2: получение управляющей операции API по ИД операции</span><span class="sxs-lookup"><span data-stu-id="51430-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="51430-113">Эта команда возвращает управляющую операцию API по ИД операции с именем Operation0003.</span><span class="sxs-lookup"><span data-stu-id="51430-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="51430-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="51430-114">PARAMETERS</span></span>

### <span data-ttu-id="51430-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="51430-115">-ApiId</span></span>
<span data-ttu-id="51430-116">Задает идентификатор операции API.</span><span class="sxs-lookup"><span data-stu-id="51430-116">Specifies the identifier of the API Operation.</span></span>

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

### <span data-ttu-id="51430-117">-Context</span><span class="sxs-lookup"><span data-stu-id="51430-117">-Context</span></span>
<span data-ttu-id="51430-118">Задает экземпляр объекта **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="51430-118">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="51430-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51430-119">-DefaultProfile</span></span>
<span data-ttu-id="51430-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="51430-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="51430-121">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="51430-121">-OperationId</span></span>
<span data-ttu-id="51430-122">Указывает идентификатор операции.</span><span class="sxs-lookup"><span data-stu-id="51430-122">Specifies the operation identifier.</span></span>

```yaml
Type: String
Parameter Sets: GetById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51430-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51430-123">CommonParameters</span></span>
<span data-ttu-id="51430-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="51430-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51430-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51430-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51430-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="51430-126">INPUTS</span></span>

### <span data-ttu-id="51430-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="51430-127">None</span></span>
<span data-ttu-id="51430-128">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="51430-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="51430-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="51430-129">OUTPUTS</span></span>

### <span data-ttu-id="51430-130">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="51430-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>
<span data-ttu-id="51430-131">Сведения об операции API в службе управления API.</span><span class="sxs-lookup"><span data-stu-id="51430-131">The details of the API Operation in Api Management service.</span></span>

### <span data-ttu-id="51430-132">IList<Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperation></span><span class="sxs-lookup"><span data-stu-id="51430-132">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation></span></span>
<span data-ttu-id="51430-133">Список операций API в службе управления API.</span><span class="sxs-lookup"><span data-stu-id="51430-133">The list of API Operation in Api Management service.</span></span>

## <span data-ttu-id="51430-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="51430-134">NOTES</span></span>

## <span data-ttu-id="51430-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="51430-135">RELATED LINKS</span></span>

[<span data-ttu-id="51430-136">New-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="51430-136">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="51430-137">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="51430-137">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)

[<span data-ttu-id="51430-138">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="51430-138">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


