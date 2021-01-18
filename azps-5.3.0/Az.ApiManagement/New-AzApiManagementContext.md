---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
ms.openlocfilehash: 060f58bc0206ea02f17239b6787f3a854aa3cb94
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98516465"
---
# <span data-ttu-id="3e641-101">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3e641-101">New-AzApiManagementContext</span></span>

## <span data-ttu-id="3e641-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e641-102">SYNOPSIS</span></span>
<span data-ttu-id="3e641-103">Создает экземпляр PsAzureApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="3e641-103">Creates an instance of PsAzureApiManagementContext.</span></span>

## <span data-ttu-id="3e641-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3e641-104">SYNTAX</span></span>

### <span data-ttu-id="3e641-105">ContextParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3e641-105">ContextParameterSet (Default)</span></span>
```
New-AzApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e641-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e641-106">ResourceIdParameterSet</span></span>
```
New-AzApiManagementContext -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e641-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e641-107">DESCRIPTION</span></span>
<span data-ttu-id="3e641-108">Для **создания экземпляра PsAzureApiManagementContext** создается экземпляр **PsAzureApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="3e641-108">The **New-AzApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="3e641-109">Этот контекст используется для всех cmdlets службы управления API.</span><span class="sxs-lookup"><span data-stu-id="3e641-109">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="3e641-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3e641-110">EXAMPLES</span></span>

### <span data-ttu-id="3e641-111">Пример 1. Создание экземпляра PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3e641-111">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="3e641-112">Эта команда создает экземпляр **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="3e641-112">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="3e641-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e641-113">PARAMETERS</span></span>

### <span data-ttu-id="3e641-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e641-114">-DefaultProfile</span></span>
<span data-ttu-id="3e641-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3e641-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e641-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e641-116">-ResourceGroupName</span></span>
<span data-ttu-id="3e641-117">Имя группы ресурсов, для которой развернута служба управления API.</span><span class="sxs-lookup"><span data-stu-id="3e641-117">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e641-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e641-118">-ResourceId</span></span>
<span data-ttu-id="3e641-119">Идентификатор ресурса Arm службы ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="3e641-119">Arm Resource Identifier of a ApiManagement service.</span></span> <span data-ttu-id="3e641-120">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="3e641-120">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e641-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3e641-121">-ServiceName</span></span>
<span data-ttu-id="3e641-122">Указывает имя развернутой службы управления API.</span><span class="sxs-lookup"><span data-stu-id="3e641-122">Specifies the name of the deployed API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e641-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e641-123">CommonParameters</span></span>
<span data-ttu-id="3e641-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e641-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e641-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e641-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e641-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3e641-126">INPUTS</span></span>

### <span data-ttu-id="3e641-127">System.String</span><span class="sxs-lookup"><span data-stu-id="3e641-127">System.String</span></span>

## <span data-ttu-id="3e641-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3e641-128">OUTPUTS</span></span>

### <span data-ttu-id="3e641-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3e641-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="3e641-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3e641-130">NOTES</span></span>

## <span data-ttu-id="3e641-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3e641-131">RELATED LINKS</span></span>
