---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOperation.md
ms.openlocfilehash: 568e3562a199a3fc247de41a30a4383bdb37adac
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404047"
---
# <span data-ttu-id="e46e0-101">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="e46e0-101">Get-AzApiManagementOperation</span></span>

## <span data-ttu-id="e46e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e46e0-102">SYNOPSIS</span></span>
<span data-ttu-id="e46e0-103">Возвращает список или указанную операцию API.</span><span class="sxs-lookup"><span data-stu-id="e46e0-103">Gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="e46e0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e46e0-104">SYNTAX</span></span>

### <span data-ttu-id="e46e0-105">GetAllApiOperations (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e46e0-105">GetAllApiOperations (Default)</span></span>
```
Get-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e46e0-106">GetById</span><span class="sxs-lookup"><span data-stu-id="e46e0-106">GetById</span></span>
```
Get-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e46e0-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e46e0-107">DESCRIPTION</span></span>
<span data-ttu-id="e46e0-108">**Get-AzApiManagementOperation** получает список или указанную операцию API.</span><span class="sxs-lookup"><span data-stu-id="e46e0-108">The **Get-AzApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="e46e0-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e46e0-109">EXAMPLES</span></span>

### <span data-ttu-id="e46e0-110">Пример 1. Получить все операции управления API</span><span class="sxs-lookup"><span data-stu-id="e46e0-110">Example 1: Get all API management operations</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOperation -Context $apimContext -ApiId $APIId
```

<span data-ttu-id="e46e0-111">Эта команда получает все операции управления API.</span><span class="sxs-lookup"><span data-stu-id="e46e0-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="e46e0-112">Пример 2. Получить операцию управления API по ИД операции</span><span class="sxs-lookup"><span data-stu-id="e46e0-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="e46e0-113">Эта команда получает операцию управления API по ИД операции Operation0003.</span><span class="sxs-lookup"><span data-stu-id="e46e0-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="e46e0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e46e0-114">PARAMETERS</span></span>

### <span data-ttu-id="e46e0-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="e46e0-115">-ApiId</span></span>
<span data-ttu-id="e46e0-116">Определяет идентификатор операции API.</span><span class="sxs-lookup"><span data-stu-id="e46e0-116">Specifies the identifier of the API Operation.</span></span>

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

### <span data-ttu-id="e46e0-117">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="e46e0-117">-ApiRevision</span></span>
<span data-ttu-id="e46e0-118">Идентификатор изменения API.</span><span class="sxs-lookup"><span data-stu-id="e46e0-118">Identifier of API Revision.</span></span> <span data-ttu-id="e46e0-119">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="e46e0-119">This parameter is optional.</span></span> <span data-ttu-id="e46e0-120">Если не указано, операция будет извлечена из активной редакции API.</span><span class="sxs-lookup"><span data-stu-id="e46e0-120">If not specified, the operation will be retrieved from the currently active api revision.</span></span>

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

### <span data-ttu-id="e46e0-121">-Контекст</span><span class="sxs-lookup"><span data-stu-id="e46e0-121">-Context</span></span>
<span data-ttu-id="e46e0-122">Указывает экземпляр объекта **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="e46e0-122">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e46e0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e46e0-123">-DefaultProfile</span></span>
<span data-ttu-id="e46e0-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e46e0-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e46e0-125">-OperationId</span><span class="sxs-lookup"><span data-stu-id="e46e0-125">-OperationId</span></span>
<span data-ttu-id="e46e0-126">Определяет идентификатор операции.</span><span class="sxs-lookup"><span data-stu-id="e46e0-126">Specifies the operation identifier.</span></span>

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

### <span data-ttu-id="e46e0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e46e0-127">CommonParameters</span></span>
<span data-ttu-id="e46e0-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e46e0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e46e0-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e46e0-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e46e0-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e46e0-130">INPUTS</span></span>

### <span data-ttu-id="e46e0-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e46e0-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e46e0-132">System.String</span><span class="sxs-lookup"><span data-stu-id="e46e0-132">System.String</span></span>

## <span data-ttu-id="e46e0-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e46e0-133">OUTPUTS</span></span>

### <span data-ttu-id="e46e0-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="e46e0-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="e46e0-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e46e0-135">NOTES</span></span>

## <span data-ttu-id="e46e0-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e46e0-136">RELATED LINKS</span></span>

[<span data-ttu-id="e46e0-137">New-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="e46e0-137">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="e46e0-138">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="e46e0-138">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)

[<span data-ttu-id="e46e0-139">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="e46e0-139">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


