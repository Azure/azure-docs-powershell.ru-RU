---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRevision.md
ms.openlocfilehash: e653053264baaa343b474f534f30915d725e5553
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990604"
---
# <span data-ttu-id="6e349-101">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="6e349-101">Get-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="6e349-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e349-102">SYNOPSIS</span></span>
<span data-ttu-id="6e349-103">Подробные сведения о всех изменениях API в API.</span><span class="sxs-lookup"><span data-stu-id="6e349-103">Gets details of all the API Revisions of an API</span></span>

## <span data-ttu-id="6e349-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6e349-104">SYNTAX</span></span>

```
Get-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e349-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e349-105">DESCRIPTION</span></span>
<span data-ttu-id="6e349-106">**Cmdlet Get-AzApiManagementApiRevision** получает сведения о всех редакциях API</span><span class="sxs-lookup"><span data-stu-id="6e349-106">The **Get-AzApiManagementApiRevision** cmdlet gets the details of all revisions of an API</span></span>

## <span data-ttu-id="6e349-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6e349-107">EXAMPLES</span></span>

### <span data-ttu-id="6e349-108">Пример 1. Все изменения API</span><span class="sxs-lookup"><span data-stu-id="6e349-108">Example 1: Get all API Revisions of an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRevision -Context $ApiMgmtContext -ApiId "5adf6fbf0faadf3ad8558065"

ApiId           : /apis/5adf6fbf0faadf3ad8558065;rev=3
ApiRevision     : 3
CreatedDateTime : 4/26/2018 10:57:42 PM
UpdatedDateTime : 4/26/2018 10:57:42 PM
Description     : ddsds
PrivateUrl      : /httpbin/v1;rev=3
IsOnline        : True
IsCurrent       : False

ApiId           : /apis/5adf6fbf0faadf3ad8558065;rev=2
ApiRevision     : 2
CreatedDateTime : 4/26/2018 10:57:33 PM
UpdatedDateTime : 4/26/2018 10:57:33 PM
Description     : AA
PrivateUrl      : /httpbin/v1
IsOnline        : True
IsCurrent       : True

ApiId           : /apis/5adf6fbf0faadf3ad8558065;rev=1
ApiRevision     : 1
CreatedDateTime : 4/24/2018 5:56:17 PM
UpdatedDateTime : 5/9/2018 9:29:06 PM
Description     :
PrivateUrl      : /httpbin/v1;rev=1
IsOnline        : True
IsCurrent       : False
```

<span data-ttu-id="6e349-109">Эта команда получает все редакцию API указанного API для конкретного контекста ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="6e349-109">This command gets all of the API revision of specified API for particular ApiManagement Context.</span></span>

## <span data-ttu-id="6e349-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e349-110">PARAMETERS</span></span>

### <span data-ttu-id="6e349-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="6e349-111">-ApiId</span></span>
<span data-ttu-id="6e349-112">Идентификатор API, редакции которого нужно перечислить.</span><span class="sxs-lookup"><span data-stu-id="6e349-112">API identifier whose revisions we want to list.</span></span>
<span data-ttu-id="6e349-113">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="6e349-113">This parameter is required.</span></span>

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

### <span data-ttu-id="6e349-114">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="6e349-114">-ApiRevision</span></span>
<span data-ttu-id="6e349-115">Идентификатор редакции определенного изменения API.</span><span class="sxs-lookup"><span data-stu-id="6e349-115">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="6e349-116">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="6e349-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="6e349-117">-Контекст</span><span class="sxs-lookup"><span data-stu-id="6e349-117">-Context</span></span>
<span data-ttu-id="6e349-118">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="6e349-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="6e349-119">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="6e349-119">This parameter is required.</span></span>

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

### <span data-ttu-id="6e349-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e349-120">-DefaultProfile</span></span>
<span data-ttu-id="6e349-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6e349-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e349-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e349-122">CommonParameters</span></span>
<span data-ttu-id="6e349-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e349-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e349-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6e349-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e349-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6e349-125">INPUTS</span></span>

### <span data-ttu-id="6e349-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6e349-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6e349-127">System.String</span><span class="sxs-lookup"><span data-stu-id="6e349-127">System.String</span></span>

## <span data-ttu-id="6e349-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6e349-128">OUTPUTS</span></span>

### <span data-ttu-id="6e349-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="6e349-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRevision</span></span>

## <span data-ttu-id="6e349-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6e349-130">NOTES</span></span>

## <span data-ttu-id="6e349-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6e349-131">RELATED LINKS</span></span>
