---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantaccesssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccessSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccessSecret.md
ms.openlocfilehash: ec64a339c29facdbb940b8141c72222ff932c1bd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391775"
---
# <span data-ttu-id="b01d3-101">Get-AzApiManagementTenantAccessSecret</span><span class="sxs-lookup"><span data-stu-id="b01d3-101">Get-AzApiManagementTenantAccessSecret</span></span>

## <span data-ttu-id="b01d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b01d3-102">SYNOPSIS</span></span>
<span data-ttu-id="b01d3-103">Получает ключи конфигурации доступа для клиента.</span><span class="sxs-lookup"><span data-stu-id="b01d3-103">Gets the access configuration keys for a tenant.</span></span>

## <span data-ttu-id="b01d3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b01d3-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccessSecret -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b01d3-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b01d3-105">DESCRIPTION</span></span>
<span data-ttu-id="b01d3-106">Получает ключи конфигурации доступа для клиента.</span><span class="sxs-lookup"><span data-stu-id="b01d3-106">Gets the access configuration keys for a tenant.</span></span>

## <span data-ttu-id="b01d3-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b01d3-107">EXAMPLES</span></span>

### <span data-ttu-id="b01d3-108">Пример 1. Получите ключи конфигурации доступа к клиенту</span><span class="sxs-lookup"><span data-stu-id="b01d3-108">Example 1: Get tenant access configuration keys</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccessSecret -Context $apimContext
```

<span data-ttu-id="b01d3-109">Эта команда получает ключи конфигурации доступа клиента для указанного контекста.</span><span class="sxs-lookup"><span data-stu-id="b01d3-109">This command gets the tenant access configuration keys for the specified context.</span></span>

## <span data-ttu-id="b01d3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b01d3-110">PARAMETERS</span></span>

### <span data-ttu-id="b01d3-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="b01d3-111">-Context</span></span>
<span data-ttu-id="b01d3-112">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b01d3-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b01d3-113">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="b01d3-113">This parameter is required.</span></span>

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

### <span data-ttu-id="b01d3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b01d3-114">-DefaultProfile</span></span>
<span data-ttu-id="b01d3-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b01d3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b01d3-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b01d3-116">CommonParameters</span></span>
<span data-ttu-id="b01d3-117">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b01d3-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b01d3-118">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b01d3-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b01d3-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b01d3-119">INPUTS</span></span>

### <span data-ttu-id="b01d3-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b01d3-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="b01d3-121">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b01d3-121">OUTPUTS</span></span>

### <span data-ttu-id="b01d3-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="b01d3-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="b01d3-123">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b01d3-123">NOTES</span></span>

## <span data-ttu-id="b01d3-124">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b01d3-124">RELATED LINKS</span></span>
