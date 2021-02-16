---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementhttpmessagediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
ms.openlocfilehash: 10c84654bb5d074ee9f668062d1fa7a18d92f8b0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100235377"
---
# <span data-ttu-id="fa943-101">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="fa943-101">New-AzApiManagementHttpMessageDiagnostic</span></span>

## <span data-ttu-id="fa943-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa943-102">SYNOPSIS</span></span>
<span data-ttu-id="fa943-103">Создание экземпляра **PsApiManagementHttpMessageDiagnostic,** который является параметром диагностики http-сообщения.</span><span class="sxs-lookup"><span data-stu-id="fa943-103">Creates an instance of **PsApiManagementHttpMessageDiagnostic** which is an Http Message diagnostic setting of the Diagnostic</span></span>

## <span data-ttu-id="fa943-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fa943-104">SYNTAX</span></span>

```
New-AzApiManagementHttpMessageDiagnostic [-HeadersToLog <String[]>] [-BodyBytesToLog <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa943-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa943-105">DESCRIPTION</span></span>
<span data-ttu-id="fa943-106">Для этого создается параметр диагностики **http-сообщения.**</span><span class="sxs-lookup"><span data-stu-id="fa943-106">The cmdlet **New-AzApiManagementHttpMessageDiagnostic** creates the Http Message diagnostic setting.</span></span>

## <span data-ttu-id="fa943-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fa943-107">EXAMPLES</span></span>

### <span data-ttu-id="fa943-108">Пример 1. Создание базового параметра диагностики http-сообщения</span><span class="sxs-lookup"><span data-stu-id="fa943-108">Example 1: Create a Basic Http Message diagnostic Setting</span></span>
```powershell
PS C:\>  New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100

Headers                   Body
-------                   ----
{Content-Type, UserAgent} Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBodyDiagnosticSetting
```

<span data-ttu-id="fa943-109">Создание параметра диагностики http-сообщения для журнала и создания его заглавных полей вместе `Content-Type` `User-Agent` со 100байтами `body`</span><span class="sxs-lookup"><span data-stu-id="fa943-109">Create a http message diagnostic setting to log `Content-Type` and `User-Agent` headers along with 100 bytes of `body`</span></span>

## <span data-ttu-id="fa943-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa943-110">PARAMETERS</span></span>

### <span data-ttu-id="fa943-111">-BodyBytesToLog</span><span class="sxs-lookup"><span data-stu-id="fa943-111">-BodyBytesToLog</span></span>
<span data-ttu-id="fa943-112">Количество вех для регистрации в теле запроса.</span><span class="sxs-lookup"><span data-stu-id="fa943-112">Number of request body bytes to log.</span></span> <span data-ttu-id="fa943-113">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="fa943-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="fa943-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa943-114">-DefaultProfile</span></span>
<span data-ttu-id="fa943-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fa943-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa943-116">-HeadersToLog</span><span class="sxs-lookup"><span data-stu-id="fa943-116">-HeadersToLog</span></span>
<span data-ttu-id="fa943-117">Массив регистраторов.</span><span class="sxs-lookup"><span data-stu-id="fa943-117">The array of headers to log.</span></span> <span data-ttu-id="fa943-118">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="fa943-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="fa943-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa943-119">CommonParameters</span></span>
<span data-ttu-id="fa943-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa943-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa943-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fa943-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa943-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fa943-122">INPUTS</span></span>

### <span data-ttu-id="fa943-123">Нет</span><span class="sxs-lookup"><span data-stu-id="fa943-123">None</span></span>

## <span data-ttu-id="fa943-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fa943-124">OUTPUTS</span></span>

### <span data-ttu-id="fa943-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="fa943-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic</span></span>

## <span data-ttu-id="fa943-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fa943-126">NOTES</span></span>

## <span data-ttu-id="fa943-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fa943-127">RELATED LINKS</span></span>

[<span data-ttu-id="fa943-128">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="fa943-128">New-AzApiManagementDiagnostic</span></span>](./New-AzApiManagementDiagnostic.md)

[<span data-ttu-id="fa943-129">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="fa943-129">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)