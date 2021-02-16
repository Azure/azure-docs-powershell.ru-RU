---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOperation.md
ms.openlocfilehash: 568e3562a199a3fc247de41a30a4383bdb37adac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239792"
---
# <span data-ttu-id="56ebb-101">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="56ebb-101">Get-AzApiManagementOperation</span></span>

## <span data-ttu-id="56ebb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56ebb-102">SYNOPSIS</span></span>
<span data-ttu-id="56ebb-103">Возвращает список или указанную операцию API.</span><span class="sxs-lookup"><span data-stu-id="56ebb-103">Gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="56ebb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="56ebb-104">SYNTAX</span></span>

### <span data-ttu-id="56ebb-105">GetAllApiOperations (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="56ebb-105">GetAllApiOperations (Default)</span></span>
```
Get-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56ebb-106">GetById</span><span class="sxs-lookup"><span data-stu-id="56ebb-106">GetById</span></span>
```
Get-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56ebb-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="56ebb-107">DESCRIPTION</span></span>
<span data-ttu-id="56ebb-108">**Get-AzApiManagementOperation** получает список или указанную операцию API.</span><span class="sxs-lookup"><span data-stu-id="56ebb-108">The **Get-AzApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="56ebb-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="56ebb-109">EXAMPLES</span></span>

### <span data-ttu-id="56ebb-110">Пример 1. Получить все операции управления API</span><span class="sxs-lookup"><span data-stu-id="56ebb-110">Example 1: Get all API management operations</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOperation -Context $apimContext -ApiId $APIId
```

<span data-ttu-id="56ebb-111">Эта команда получает все операции управления API.</span><span class="sxs-lookup"><span data-stu-id="56ebb-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="56ebb-112">Пример 2. Получить операцию управления API по ИД операции</span><span class="sxs-lookup"><span data-stu-id="56ebb-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="56ebb-113">Эта команда получает операцию управления API по ИД операции Operation0003.</span><span class="sxs-lookup"><span data-stu-id="56ebb-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="56ebb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56ebb-114">PARAMETERS</span></span>

### <span data-ttu-id="56ebb-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="56ebb-115">-ApiId</span></span>
<span data-ttu-id="56ebb-116">Определяет идентификатор операции API.</span><span class="sxs-lookup"><span data-stu-id="56ebb-116">Specifies the identifier of the API Operation.</span></span>

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

### <span data-ttu-id="56ebb-117">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="56ebb-117">-ApiRevision</span></span>
<span data-ttu-id="56ebb-118">Идентификатор изменения API.</span><span class="sxs-lookup"><span data-stu-id="56ebb-118">Identifier of API Revision.</span></span> <span data-ttu-id="56ebb-119">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="56ebb-119">This parameter is optional.</span></span> <span data-ttu-id="56ebb-120">Если не указано, операция будет извлечена из активной редакции API.</span><span class="sxs-lookup"><span data-stu-id="56ebb-120">If not specified, the operation will be retrieved from the currently active api revision.</span></span>

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

### <span data-ttu-id="56ebb-121">-Контекст</span><span class="sxs-lookup"><span data-stu-id="56ebb-121">-Context</span></span>
<span data-ttu-id="56ebb-122">Указывает экземпляр объекта **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="56ebb-122">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="56ebb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56ebb-123">-DefaultProfile</span></span>
<span data-ttu-id="56ebb-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="56ebb-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56ebb-125">-OperationId</span><span class="sxs-lookup"><span data-stu-id="56ebb-125">-OperationId</span></span>
<span data-ttu-id="56ebb-126">Определяет идентификатор операции.</span><span class="sxs-lookup"><span data-stu-id="56ebb-126">Specifies the operation identifier.</span></span>

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

### <span data-ttu-id="56ebb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56ebb-127">CommonParameters</span></span>
<span data-ttu-id="56ebb-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56ebb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56ebb-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56ebb-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56ebb-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="56ebb-130">INPUTS</span></span>

### <span data-ttu-id="56ebb-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="56ebb-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="56ebb-132">System.String</span><span class="sxs-lookup"><span data-stu-id="56ebb-132">System.String</span></span>

## <span data-ttu-id="56ebb-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="56ebb-133">OUTPUTS</span></span>

### <span data-ttu-id="56ebb-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="56ebb-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="56ebb-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="56ebb-135">NOTES</span></span>

## <span data-ttu-id="56ebb-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="56ebb-136">RELATED LINKS</span></span>

[<span data-ttu-id="56ebb-137">New-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="56ebb-137">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="56ebb-138">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="56ebb-138">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)

[<span data-ttu-id="56ebb-139">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="56ebb-139">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


