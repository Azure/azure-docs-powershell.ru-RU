---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementpipelinediagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
ms.openlocfilehash: 7e6f6515b24a7cefabd40a6fdfaedfda430f69d0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066692"
---
# <span data-ttu-id="732b3-101">New-AzApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="732b3-101">New-AzApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="732b3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="732b3-102">SYNOPSIS</span></span>
<span data-ttu-id="732b3-103">Создайте параметры диагностики для входящих и исходящих HTTP-сообщений на шлюзе.</span><span class="sxs-lookup"><span data-stu-id="732b3-103">Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="732b3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="732b3-104">SYNTAX</span></span>

```
New-AzApiManagementPipelineDiagnosticSetting [-Request <PsApiManagementHttpMessageDiagnostic>]
 [-Response <PsApiManagementHttpMessageDiagnostic>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="732b3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="732b3-105">DESCRIPTION</span></span>
<span data-ttu-id="732b3-106">Командлет **New-AzApiManagementPipelineDiagnosticSetting** создает параметры диагностики для входящих и исходящих HTTP-сообщений на шлюзе.</span><span class="sxs-lookup"><span data-stu-id="732b3-106">The cmdlet **New-AzApiManagementPipelineDiagnosticSetting** creates the Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="732b3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="732b3-107">EXAMPLES</span></span>

### <span data-ttu-id="732b3-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="732b3-108">Example 1</span></span>
```powershell
PS c:\> $httpMessageDiagnostic = New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100
PS c:\> New-AzApiManagementPipelineDiagnosticSetting -Request $httpMessageDiagnostic -Response $httpMessageDiagnostic

Request                                                                                              Response
-------                                                                                              --------
Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
```

<span data-ttu-id="732b3-109">Создание диагностики конвейера для использования на веб-интерфейсе или внутреннем объекте в диагностике.</span><span class="sxs-lookup"><span data-stu-id="732b3-109">Create a pipeline diagnostic to be used in either FrontEnd or Backend in the Diagnostic Entity.</span></span>

## <span data-ttu-id="732b3-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="732b3-110">PARAMETERS</span></span>

### <span data-ttu-id="732b3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="732b3-111">-DefaultProfile</span></span>
<span data-ttu-id="732b3-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="732b3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="732b3-113">-Request</span><span class="sxs-lookup"><span data-stu-id="732b3-113">-Request</span></span>
<span data-ttu-id="732b3-114">Параметр диагностики для запроса.</span><span class="sxs-lookup"><span data-stu-id="732b3-114">Diagnostic setting for Request.</span></span>
<span data-ttu-id="732b3-115">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="732b3-115">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="732b3-116">-Ответ</span><span class="sxs-lookup"><span data-stu-id="732b3-116">-Response</span></span>
<span data-ttu-id="732b3-117">Параметр диагностики для ответа.</span><span class="sxs-lookup"><span data-stu-id="732b3-117">Diagnostic setting for Response.</span></span>
<span data-ttu-id="732b3-118">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="732b3-118">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="732b3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="732b3-119">CommonParameters</span></span>
<span data-ttu-id="732b3-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="732b3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="732b3-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="732b3-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="732b3-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="732b3-122">INPUTS</span></span>

### <span data-ttu-id="732b3-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="732b3-123">None</span></span>

## <span data-ttu-id="732b3-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="732b3-124">OUTPUTS</span></span>

### <span data-ttu-id="732b3-125">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="732b3-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="732b3-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="732b3-126">NOTES</span></span>

## <span data-ttu-id="732b3-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="732b3-127">RELATED LINKS</span></span>

[<span data-ttu-id="732b3-128">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="732b3-128">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="732b3-129">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="732b3-129">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="732b3-130">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="732b3-130">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="732b3-131">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="732b3-131">New-AzApiManagementHttpMessageDiagnostic</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)


