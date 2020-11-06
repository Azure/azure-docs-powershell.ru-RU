---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApiRevision.md
ms.openlocfilehash: f57a95e97c0ec74e7e45338e15a028feab60849b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565982"
---
# <span data-ttu-id="d525d-101">Get-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="d525d-101">Get-AzureRmApiManagementApiRevision</span></span>

## <span data-ttu-id="d525d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d525d-102">SYNOPSIS</span></span>
<span data-ttu-id="d525d-103">Получение подробных сведений о всех редакциях API для API</span><span class="sxs-lookup"><span data-stu-id="d525d-103">Gets details of all the API Revisions of an API</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d525d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d525d-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d525d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d525d-105">DESCRIPTION</span></span>
<span data-ttu-id="d525d-106">Командлет **Get-AzureRmApiManagementApiRevision** получает подробные сведения обо всех РЕДАКЦИЯх API.</span><span class="sxs-lookup"><span data-stu-id="d525d-106">The **Get-AzureRmApiManagementApiRevision** cmdlet gets the details of all revisions of an API</span></span>

## <span data-ttu-id="d525d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d525d-107">EXAMPLES</span></span>

### <span data-ttu-id="d525d-108">Пример 1: получение всех редакций API для API</span><span class="sxs-lookup"><span data-stu-id="d525d-108">Example 1: Get all API Revisions of an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApiRevision -Context $ApiMgmtContext -ApiId "5adf6fbf0faadf3ad8558065"

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

<span data-ttu-id="d525d-109">Эта команда возвращает все редакции API указанного API для определенного контекста ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="d525d-109">This command gets all of the API revision of specified API for particular ApiManagement Context.</span></span>

## <span data-ttu-id="d525d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d525d-110">PARAMETERS</span></span>

### <span data-ttu-id="d525d-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="d525d-111">-ApiId</span></span>
<span data-ttu-id="d525d-112">Идентификатор API, для которого нужно создать список исправлений.</span><span class="sxs-lookup"><span data-stu-id="d525d-112">API identifier whose revisions we want to list.</span></span>
<span data-ttu-id="d525d-113">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="d525d-113">This parameter is required.</span></span>

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

### <span data-ttu-id="d525d-114">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="d525d-114">-ApiRevision</span></span>
<span data-ttu-id="d525d-115">Идентификатор редакции определенной редакции API.</span><span class="sxs-lookup"><span data-stu-id="d525d-115">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="d525d-116">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="d525d-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="d525d-117">-Context</span><span class="sxs-lookup"><span data-stu-id="d525d-117">-Context</span></span>
<span data-ttu-id="d525d-118">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d525d-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d525d-119">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="d525d-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d525d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d525d-120">-DefaultProfile</span></span>
<span data-ttu-id="d525d-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d525d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d525d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d525d-122">CommonParameters</span></span>
<span data-ttu-id="d525d-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d525d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d525d-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d525d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d525d-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d525d-125">INPUTS</span></span>

### <span data-ttu-id="d525d-126">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d525d-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d525d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d525d-127">System.String</span></span>

## <span data-ttu-id="d525d-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d525d-128">OUTPUTS</span></span>

### <span data-ttu-id="d525d-129">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="d525d-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRevision</span></span>

## <span data-ttu-id="d525d-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="d525d-130">NOTES</span></span>

## <span data-ttu-id="d525d-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d525d-131">RELATED LINKS</span></span>
