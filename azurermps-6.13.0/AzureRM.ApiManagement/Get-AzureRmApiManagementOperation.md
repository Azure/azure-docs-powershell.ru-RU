---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
ms.openlocfilehash: 469d10303f286a0feca162e628a1564826b850d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556984"
---
# <span data-ttu-id="917b6-101">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="917b6-101">Get-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="917b6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="917b6-102">SYNOPSIS</span></span>
<span data-ttu-id="917b6-103">Возвращает список или указанную операцию API.</span><span class="sxs-lookup"><span data-stu-id="917b6-103">Gets a list or a specified API Operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="917b6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="917b6-104">SYNTAX</span></span>

### <span data-ttu-id="917b6-105">GetAllApiOperations (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="917b6-105">GetAllApiOperations (Default)</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="917b6-106">GetById</span><span class="sxs-lookup"><span data-stu-id="917b6-106">GetById</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="917b6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="917b6-107">DESCRIPTION</span></span>
<span data-ttu-id="917b6-108">Функция **Get-AzureRmApiManagementOperation** возвращает список или указанную операцию API.</span><span class="sxs-lookup"><span data-stu-id="917b6-108">The **Get-AzureRmApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="917b6-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="917b6-109">EXAMPLES</span></span>

### <span data-ttu-id="917b6-110">Пример 1: получение всех операций управления API</span><span class="sxs-lookup"><span data-stu-id="917b6-110">Example 1: Get all API management operations</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIId
```

<span data-ttu-id="917b6-111">Эта команда получает все операции по управлению API.</span><span class="sxs-lookup"><span data-stu-id="917b6-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="917b6-112">Пример 2: получение управляющей операции API по ИД операции</span><span class="sxs-lookup"><span data-stu-id="917b6-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="917b6-113">Эта команда возвращает управляющую операцию API по ИД операции с именем Operation0003.</span><span class="sxs-lookup"><span data-stu-id="917b6-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="917b6-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="917b6-114">PARAMETERS</span></span>

### <span data-ttu-id="917b6-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="917b6-115">-ApiId</span></span>
<span data-ttu-id="917b6-116">Задает идентификатор операции API.</span><span class="sxs-lookup"><span data-stu-id="917b6-116">Specifies the identifier of the API Operation.</span></span>

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

### <span data-ttu-id="917b6-117">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="917b6-117">-ApiRevision</span></span>
<span data-ttu-id="917b6-118">Идентификатор редакции API.</span><span class="sxs-lookup"><span data-stu-id="917b6-118">Identifier of API Revision.</span></span> <span data-ttu-id="917b6-119">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="917b6-119">This parameter is optional.</span></span> <span data-ttu-id="917b6-120">Если не указано, операция будет получена из текущей активной версии API.</span><span class="sxs-lookup"><span data-stu-id="917b6-120">If not specified, the operation will be retrieved from the currently active api revision.</span></span>

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

### <span data-ttu-id="917b6-121">-Context</span><span class="sxs-lookup"><span data-stu-id="917b6-121">-Context</span></span>
<span data-ttu-id="917b6-122">Задает экземпляр объекта **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="917b6-122">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="917b6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="917b6-123">-DefaultProfile</span></span>
<span data-ttu-id="917b6-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="917b6-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="917b6-125">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="917b6-125">-OperationId</span></span>
<span data-ttu-id="917b6-126">Указывает идентификатор операции.</span><span class="sxs-lookup"><span data-stu-id="917b6-126">Specifies the operation identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="917b6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="917b6-127">CommonParameters</span></span>
<span data-ttu-id="917b6-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="917b6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="917b6-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="917b6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="917b6-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="917b6-130">INPUTS</span></span>

### <span data-ttu-id="917b6-131">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="917b6-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="917b6-132">System. String</span><span class="sxs-lookup"><span data-stu-id="917b6-132">System.String</span></span>

## <span data-ttu-id="917b6-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="917b6-133">OUTPUTS</span></span>

### <span data-ttu-id="917b6-134">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="917b6-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="917b6-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="917b6-135">NOTES</span></span>

## <span data-ttu-id="917b6-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="917b6-136">RELATED LINKS</span></span>

[<span data-ttu-id="917b6-137">New-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="917b6-137">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="917b6-138">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="917b6-138">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)

[<span data-ttu-id="917b6-139">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="917b6-139">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


