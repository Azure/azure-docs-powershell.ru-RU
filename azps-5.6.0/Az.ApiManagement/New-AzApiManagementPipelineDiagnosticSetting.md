---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementpipelinediagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
ms.openlocfilehash: e68449a84bb64454291434bded40ed2e494fdab4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979048"
---
# <span data-ttu-id="dc6c8-101">New-AzApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="dc6c8-101">New-AzApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="dc6c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc6c8-102">SYNOPSIS</span></span>
<span data-ttu-id="dc6c8-103">Создание диагностических параметров для входящих и исходяющих HTTP-сообщений шлюзу.</span><span class="sxs-lookup"><span data-stu-id="dc6c8-103">Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="dc6c8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dc6c8-104">SYNTAX</span></span>

```
New-AzApiManagementPipelineDiagnosticSetting [-Request <PsApiManagementHttpMessageDiagnostic>]
 [-Response <PsApiManagementHttpMessageDiagnostic>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dc6c8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc6c8-105">DESCRIPTION</span></span>
<span data-ttu-id="dc6c8-106">Для шлюза с помощью cmdlet **New-AzApiManagementPipelineDiagnosticSetting** создаются параметры диагностики для входящих и исходяющих HTTP-сообщений.</span><span class="sxs-lookup"><span data-stu-id="dc6c8-106">The cmdlet **New-AzApiManagementPipelineDiagnosticSetting** creates the Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="dc6c8-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dc6c8-107">EXAMPLES</span></span>

### <span data-ttu-id="dc6c8-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dc6c8-108">Example 1</span></span>
```powershell
PS c:\> $httpMessageDiagnostic = New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100
PS c:\> New-AzApiManagementPipelineDiagnosticSetting -Request $httpMessageDiagnostic -Response $httpMessageDiagnostic

Request                                                                                              Response
-------                                                                                              --------
Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
```

<span data-ttu-id="dc6c8-109">Создайте диагностику конвейера для использования в FrontEnd или Backend в объекте диагностики.</span><span class="sxs-lookup"><span data-stu-id="dc6c8-109">Create a pipeline diagnostic to be used in either FrontEnd or Backend in the Diagnostic Entity.</span></span>

## <span data-ttu-id="dc6c8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc6c8-110">PARAMETERS</span></span>

### <span data-ttu-id="dc6c8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc6c8-111">-DefaultProfile</span></span>
<span data-ttu-id="dc6c8-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dc6c8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc6c8-113">-Request</span><span class="sxs-lookup"><span data-stu-id="dc6c8-113">-Request</span></span>
<span data-ttu-id="dc6c8-114">Параметр диагностики запроса.</span><span class="sxs-lookup"><span data-stu-id="dc6c8-114">Diagnostic setting for Request.</span></span>
<span data-ttu-id="dc6c8-115">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="dc6c8-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="dc6c8-116">-Response</span><span class="sxs-lookup"><span data-stu-id="dc6c8-116">-Response</span></span>
<span data-ttu-id="dc6c8-117">Параметр диагностики для ответа.</span><span class="sxs-lookup"><span data-stu-id="dc6c8-117">Diagnostic setting for Response.</span></span>
<span data-ttu-id="dc6c8-118">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="dc6c8-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="dc6c8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc6c8-119">CommonParameters</span></span>
<span data-ttu-id="dc6c8-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc6c8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc6c8-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dc6c8-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc6c8-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dc6c8-122">INPUTS</span></span>

### <span data-ttu-id="dc6c8-123">Нет</span><span class="sxs-lookup"><span data-stu-id="dc6c8-123">None</span></span>

## <span data-ttu-id="dc6c8-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dc6c8-124">OUTPUTS</span></span>

### <span data-ttu-id="dc6c8-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="dc6c8-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="dc6c8-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dc6c8-126">NOTES</span></span>

## <span data-ttu-id="dc6c8-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc6c8-127">RELATED LINKS</span></span>

[<span data-ttu-id="dc6c8-128">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="dc6c8-128">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="dc6c8-129">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="dc6c8-129">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="dc6c8-130">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="dc6c8-130">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="dc6c8-131">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="dc6c8-131">New-AzApiManagementHttpMessageDiagnostic</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)


