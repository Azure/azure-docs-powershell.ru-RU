---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementhttpmessagediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
ms.openlocfilehash: 3475778104655e6b27061edf08ced376f192ea34
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988543"
---
# <span data-ttu-id="e0092-101">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="e0092-101">New-AzApiManagementHttpMessageDiagnostic</span></span>

## <span data-ttu-id="e0092-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0092-102">SYNOPSIS</span></span>
<span data-ttu-id="e0092-103">Создание экземпляра **PsApiManagementHttpMessageDiagnostic,** который является параметром диагностики http-сообщения</span><span class="sxs-lookup"><span data-stu-id="e0092-103">Creates an instance of **PsApiManagementHttpMessageDiagnostic** which is an Http Message diagnostic setting of the Diagnostic</span></span>

## <span data-ttu-id="e0092-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e0092-104">SYNTAX</span></span>

```
New-AzApiManagementHttpMessageDiagnostic [-HeadersToLog <String[]>] [-BodyBytesToLog <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0092-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0092-105">DESCRIPTION</span></span>
<span data-ttu-id="e0092-106">Для этого создается параметр диагностики **http-сообщения.**</span><span class="sxs-lookup"><span data-stu-id="e0092-106">The cmdlet **New-AzApiManagementHttpMessageDiagnostic** creates the Http Message diagnostic setting.</span></span>

## <span data-ttu-id="e0092-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e0092-107">EXAMPLES</span></span>

### <span data-ttu-id="e0092-108">Пример 1. Создание базового параметра диагностики http-сообщения</span><span class="sxs-lookup"><span data-stu-id="e0092-108">Example 1: Create a Basic Http Message diagnostic Setting</span></span>
```powershell
PS C:\>  New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100

Headers                   Body
-------                   ----
{Content-Type, UserAgent} Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBodyDiagnosticSetting
```

<span data-ttu-id="e0092-109">Создание параметра диагностики http-сообщения для журнала и создания его заглавных полей вместе `Content-Type` `User-Agent` со 100байтами `body`</span><span class="sxs-lookup"><span data-stu-id="e0092-109">Create a http message diagnostic setting to log `Content-Type` and `User-Agent` headers along with 100 bytes of `body`</span></span>

## <span data-ttu-id="e0092-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0092-110">PARAMETERS</span></span>

### <span data-ttu-id="e0092-111">-BodyBytesToLog</span><span class="sxs-lookup"><span data-stu-id="e0092-111">-BodyBytesToLog</span></span>
<span data-ttu-id="e0092-112">Количество в журналебайтов тела запроса.</span><span class="sxs-lookup"><span data-stu-id="e0092-112">Number of request body bytes to log.</span></span> <span data-ttu-id="e0092-113">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="e0092-113">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0092-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0092-114">-DefaultProfile</span></span>
<span data-ttu-id="e0092-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e0092-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0092-116">-HeadersToLog</span><span class="sxs-lookup"><span data-stu-id="e0092-116">-HeadersToLog</span></span>
<span data-ttu-id="e0092-117">Массив регистраторов.</span><span class="sxs-lookup"><span data-stu-id="e0092-117">The array of headers to log.</span></span> <span data-ttu-id="e0092-118">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="e0092-118">This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0092-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0092-119">CommonParameters</span></span>
<span data-ttu-id="e0092-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0092-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0092-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0092-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0092-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e0092-122">INPUTS</span></span>

### <span data-ttu-id="e0092-123">Нет</span><span class="sxs-lookup"><span data-stu-id="e0092-123">None</span></span>

## <span data-ttu-id="e0092-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e0092-124">OUTPUTS</span></span>

### <span data-ttu-id="e0092-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="e0092-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic</span></span>

## <span data-ttu-id="e0092-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e0092-126">NOTES</span></span>

## <span data-ttu-id="e0092-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e0092-127">RELATED LINKS</span></span>

[<span data-ttu-id="e0092-128">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="e0092-128">New-AzApiManagementDiagnostic</span></span>](./New-AzApiManagementDiagnostic.md)

[<span data-ttu-id="e0092-129">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="e0092-129">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)