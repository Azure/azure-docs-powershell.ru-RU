---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOperation.md
ms.openlocfilehash: 568e3562a199a3fc247de41a30a4383bdb37adac
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066399"
---
# <span data-ttu-id="d17d1-101">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d17d1-101">Get-AzApiManagementOperation</span></span>

## <span data-ttu-id="d17d1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d17d1-102">SYNOPSIS</span></span>
<span data-ttu-id="d17d1-103">Возвращает список или указанную операцию API.</span><span class="sxs-lookup"><span data-stu-id="d17d1-103">Gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="d17d1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d17d1-104">SYNTAX</span></span>

### <span data-ttu-id="d17d1-105">GetAllApiOperations (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d17d1-105">GetAllApiOperations (Default)</span></span>
```
Get-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d17d1-106">GetById</span><span class="sxs-lookup"><span data-stu-id="d17d1-106">GetById</span></span>
```
Get-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d17d1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d17d1-107">DESCRIPTION</span></span>
<span data-ttu-id="d17d1-108">Функция **Get-AzApiManagementOperation** возвращает список или указанную операцию API.</span><span class="sxs-lookup"><span data-stu-id="d17d1-108">The **Get-AzApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="d17d1-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d17d1-109">EXAMPLES</span></span>

### <span data-ttu-id="d17d1-110">Пример 1: получение всех операций управления API</span><span class="sxs-lookup"><span data-stu-id="d17d1-110">Example 1: Get all API management operations</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOperation -Context $apimContext -ApiId $APIId
```

<span data-ttu-id="d17d1-111">Эта команда получает все операции по управлению API.</span><span class="sxs-lookup"><span data-stu-id="d17d1-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="d17d1-112">Пример 2: получение управляющей операции API по ИД операции</span><span class="sxs-lookup"><span data-stu-id="d17d1-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="d17d1-113">Эта команда возвращает управляющую операцию API по ИД операции с именем Operation0003.</span><span class="sxs-lookup"><span data-stu-id="d17d1-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="d17d1-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d17d1-114">PARAMETERS</span></span>

### <span data-ttu-id="d17d1-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="d17d1-115">-ApiId</span></span>
<span data-ttu-id="d17d1-116">Задает идентификатор операции API.</span><span class="sxs-lookup"><span data-stu-id="d17d1-116">Specifies the identifier of the API Operation.</span></span>

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

### <span data-ttu-id="d17d1-117">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="d17d1-117">-ApiRevision</span></span>
<span data-ttu-id="d17d1-118">Идентификатор редакции API.</span><span class="sxs-lookup"><span data-stu-id="d17d1-118">Identifier of API Revision.</span></span> <span data-ttu-id="d17d1-119">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="d17d1-119">This parameter is optional.</span></span> <span data-ttu-id="d17d1-120">Если не указано, операция будет получена из текущей активной версии API.</span><span class="sxs-lookup"><span data-stu-id="d17d1-120">If not specified, the operation will be retrieved from the currently active api revision.</span></span>

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

### <span data-ttu-id="d17d1-121">-Context</span><span class="sxs-lookup"><span data-stu-id="d17d1-121">-Context</span></span>
<span data-ttu-id="d17d1-122">Задает экземпляр объекта **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="d17d1-122">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d17d1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d17d1-123">-DefaultProfile</span></span>
<span data-ttu-id="d17d1-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d17d1-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d17d1-125">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="d17d1-125">-OperationId</span></span>
<span data-ttu-id="d17d1-126">Указывает идентификатор операции.</span><span class="sxs-lookup"><span data-stu-id="d17d1-126">Specifies the operation identifier.</span></span>

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

### <span data-ttu-id="d17d1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d17d1-127">CommonParameters</span></span>
<span data-ttu-id="d17d1-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d17d1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d17d1-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d17d1-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d17d1-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d17d1-130">INPUTS</span></span>

### <span data-ttu-id="d17d1-131">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d17d1-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d17d1-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d17d1-132">System.String</span></span>

## <span data-ttu-id="d17d1-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d17d1-133">OUTPUTS</span></span>

### <span data-ttu-id="d17d1-134">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d17d1-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="d17d1-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="d17d1-135">NOTES</span></span>

## <span data-ttu-id="d17d1-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d17d1-136">RELATED LINKS</span></span>

[<span data-ttu-id="d17d1-137">New-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d17d1-137">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="d17d1-138">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d17d1-138">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)

[<span data-ttu-id="d17d1-139">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d17d1-139">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


