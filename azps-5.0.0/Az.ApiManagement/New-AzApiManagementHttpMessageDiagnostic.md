---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementhttpmessagediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
ms.openlocfilehash: 10c84654bb5d074ee9f668062d1fa7a18d92f8b0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246938"
---
# <span data-ttu-id="c5309-101">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c5309-101">New-AzApiManagementHttpMessageDiagnostic</span></span>

## <span data-ttu-id="c5309-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c5309-102">SYNOPSIS</span></span>
<span data-ttu-id="c5309-103">Создает экземпляр **PsApiManagementHttpMessageDiagnostic** , который является параметром диагностики HTTP-сообщений для диагностики.</span><span class="sxs-lookup"><span data-stu-id="c5309-103">Creates an instance of **PsApiManagementHttpMessageDiagnostic** which is an Http Message diagnostic setting of the Diagnostic</span></span>

## <span data-ttu-id="c5309-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c5309-104">SYNTAX</span></span>

```
New-AzApiManagementHttpMessageDiagnostic [-HeadersToLog <String[]>] [-BodyBytesToLog <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5309-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5309-105">DESCRIPTION</span></span>
<span data-ttu-id="c5309-106">Командлет **New-AzApiManagementHttpMessageDiagnostic** создает параметр диагностики HTTP-сообщений.</span><span class="sxs-lookup"><span data-stu-id="c5309-106">The cmdlet **New-AzApiManagementHttpMessageDiagnostic** creates the Http Message diagnostic setting.</span></span>

## <span data-ttu-id="c5309-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c5309-107">EXAMPLES</span></span>

### <span data-ttu-id="c5309-108">Пример 1: создание основного параметра диагностики HTTP-сообщений</span><span class="sxs-lookup"><span data-stu-id="c5309-108">Example 1: Create a Basic Http Message diagnostic Setting</span></span>
```powershell
PS C:\>  New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100

Headers                   Body
-------                   ----
{Content-Type, UserAgent} Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBodyDiagnosticSetting
```

<span data-ttu-id="c5309-109">Создание параметров диагностики сообщений HTTP для ведения журнала `Content-Type` и `User-Agent` заголовков вместе с 100 байтами `body`</span><span class="sxs-lookup"><span data-stu-id="c5309-109">Create a http message diagnostic setting to log `Content-Type` and `User-Agent` headers along with 100 bytes of `body`</span></span>

## <span data-ttu-id="c5309-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c5309-110">PARAMETERS</span></span>

### <span data-ttu-id="c5309-111">-BodyBytesToLog</span><span class="sxs-lookup"><span data-stu-id="c5309-111">-BodyBytesToLog</span></span>
<span data-ttu-id="c5309-112">Количество байтов основного текста запроса, которые нужно записать в журнал.</span><span class="sxs-lookup"><span data-stu-id="c5309-112">Number of request body bytes to log.</span></span> <span data-ttu-id="c5309-113">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c5309-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="c5309-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5309-114">-DefaultProfile</span></span>
<span data-ttu-id="c5309-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c5309-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5309-116">-HeadersToLog</span><span class="sxs-lookup"><span data-stu-id="c5309-116">-HeadersToLog</span></span>
<span data-ttu-id="c5309-117">Массив заголовков, которые нужно записать в журнал.</span><span class="sxs-lookup"><span data-stu-id="c5309-117">The array of headers to log.</span></span> <span data-ttu-id="c5309-118">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c5309-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="c5309-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5309-119">CommonParameters</span></span>
<span data-ttu-id="c5309-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c5309-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5309-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5309-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5309-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c5309-122">INPUTS</span></span>

### <span data-ttu-id="c5309-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="c5309-123">None</span></span>

## <span data-ttu-id="c5309-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5309-124">OUTPUTS</span></span>

### <span data-ttu-id="c5309-125">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c5309-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic</span></span>

## <span data-ttu-id="c5309-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="c5309-126">NOTES</span></span>

## <span data-ttu-id="c5309-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c5309-127">RELATED LINKS</span></span>

[<span data-ttu-id="c5309-128">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c5309-128">New-AzApiManagementDiagnostic</span></span>](./New-AzApiManagementDiagnostic.md)

[<span data-ttu-id="c5309-129">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="c5309-129">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)