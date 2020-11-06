---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
ms.openlocfilehash: b2c623d46dcc2d84e2c90ae5f3d94cfb54f7224a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565759"
---
# <span data-ttu-id="d3ac1-101">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d3ac1-101">Get-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="d3ac1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d3ac1-102">SYNOPSIS</span></span>
<span data-ttu-id="d3ac1-103">Возвращает список или указанную операцию API.</span><span class="sxs-lookup"><span data-stu-id="d3ac1-103">Gets a list or a specified API Operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3ac1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d3ac1-104">SYNTAX</span></span>

### <span data-ttu-id="d3ac1-105">Все операции API (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d3ac1-105">All API Operations (Default)</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3ac1-106">Найти по ИДЕНТИФИКАТОРу</span><span class="sxs-lookup"><span data-stu-id="d3ac1-106">Find by ID</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3ac1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3ac1-107">DESCRIPTION</span></span>
<span data-ttu-id="d3ac1-108">Функция **Get-AzureRmApiManagementOperation** возвращает список или указанную операцию API.</span><span class="sxs-lookup"><span data-stu-id="d3ac1-108">The **Get-AzureRmApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="d3ac1-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d3ac1-109">EXAMPLES</span></span>

### <span data-ttu-id="d3ac1-110">Пример 1: получение всех операций управления API</span><span class="sxs-lookup"><span data-stu-id="d3ac1-110">Example 1: Get all API management operations</span></span>
```
PS C:\>Get-AzureRmApiManagementOperation -Context $APImContext -ApiId $APIId
```

<span data-ttu-id="d3ac1-111">Эта команда получает все операции по управлению API.</span><span class="sxs-lookup"><span data-stu-id="d3ac1-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="d3ac1-112">Пример 2: получение управляющей операции API по ИД операции</span><span class="sxs-lookup"><span data-stu-id="d3ac1-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>Get-AzureRmApiManagementOperation -Context $APImContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="d3ac1-113">Эта команда возвращает управляющую операцию API по ИД операции с именем Operation0003.</span><span class="sxs-lookup"><span data-stu-id="d3ac1-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="d3ac1-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d3ac1-114">PARAMETERS</span></span>

### <span data-ttu-id="d3ac1-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="d3ac1-115">-ApiId</span></span>
<span data-ttu-id="d3ac1-116">Задает идентификатор операции API.</span><span class="sxs-lookup"><span data-stu-id="d3ac1-116">Specifies the identifier of the API Operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3ac1-117">-Context</span><span class="sxs-lookup"><span data-stu-id="d3ac1-117">-Context</span></span>
<span data-ttu-id="d3ac1-118">Задает экземпляр объекта **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="d3ac1-118">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d3ac1-119">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="d3ac1-119">-OperationId</span></span>
<span data-ttu-id="d3ac1-120">Указывает идентификатор операции.</span><span class="sxs-lookup"><span data-stu-id="d3ac1-120">Specifies the operation identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Find by ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3ac1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3ac1-121">-DefaultProfile</span></span>
<span data-ttu-id="d3ac1-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d3ac1-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3ac1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3ac1-123">CommonParameters</span></span>
<span data-ttu-id="d3ac1-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d3ac1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3ac1-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3ac1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3ac1-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d3ac1-126">INPUTS</span></span>

## <span data-ttu-id="d3ac1-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3ac1-127">OUTPUTS</span></span>

### <span data-ttu-id="d3ac1-128">IList<Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperation></span><span class="sxs-lookup"><span data-stu-id="d3ac1-128">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation></span></span>

## <span data-ttu-id="d3ac1-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="d3ac1-129">NOTES</span></span>

## <span data-ttu-id="d3ac1-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d3ac1-130">RELATED LINKS</span></span>

[<span data-ttu-id="d3ac1-131">New-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d3ac1-131">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="d3ac1-132">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d3ac1-132">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)

[<span data-ttu-id="d3ac1-133">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d3ac1-133">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


