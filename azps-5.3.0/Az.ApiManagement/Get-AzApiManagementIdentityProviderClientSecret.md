---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityproviderclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProviderClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProviderClientSecret.md
ms.openlocfilehash: d75d385bc158e0855601d3432dff79b2e4339f2f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98516605"
---
# <span data-ttu-id="b6b8d-101">Get-AzApiManagementIdentityProviderClientSecret</span><span class="sxs-lookup"><span data-stu-id="b6b8d-101">Get-AzApiManagementIdentityProviderClientSecret</span></span>

## <span data-ttu-id="b6b8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6b8d-102">SYNOPSIS</span></span>
<span data-ttu-id="b6b8d-103">Получите секрет клиента поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="b6b8d-103">Get the identity provider client secret.</span></span>

## <span data-ttu-id="b6b8d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b6b8d-104">SYNTAX</span></span>

```
Get-AzApiManagementIdentityProviderClientSecret -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6b8d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6b8d-105">DESCRIPTION</span></span>
<span data-ttu-id="b6b8d-106">Получите секрет клиента поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="b6b8d-106">Get the identity provider client secret.</span></span>

## <span data-ttu-id="b6b8d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b6b8d-107">EXAMPLES</span></span>

### <span data-ttu-id="b6b8d-108">Пример 1. Секрет клиента поставщика удостоверений типа AAD</span><span class="sxs-lookup"><span data-stu-id="b6b8d-108">Example 1: Get the client secret of AAD Type Identity Provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Get-AzApiManagementIdentityProviderClientSecret -Context $apimContext -Type Aad
```

<span data-ttu-id="b6b8d-109">Секрет клиента в конфигурации поставщика удостоверений Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b6b8d-109">Gets the client secret of the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="b6b8d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6b8d-110">PARAMETERS</span></span>

### <span data-ttu-id="b6b8d-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="b6b8d-111">-Context</span></span>
<span data-ttu-id="b6b8d-112">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b6b8d-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b6b8d-113">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="b6b8d-113">This parameter is required.</span></span>

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

### <span data-ttu-id="b6b8d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6b8d-114">-DefaultProfile</span></span>
<span data-ttu-id="b6b8d-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b6b8d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6b8d-116">-Type</span><span class="sxs-lookup"><span data-stu-id="b6b8d-116">-Type</span></span>
<span data-ttu-id="b6b8d-117">Идентификатор поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="b6b8d-117">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="b6b8d-118">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="b6b8d-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6b8d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6b8d-119">CommonParameters</span></span>
<span data-ttu-id="b6b8d-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6b8d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6b8d-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b6b8d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6b8d-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b6b8d-122">INPUTS</span></span>

### <span data-ttu-id="b6b8d-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b6b8d-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b6b8d-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="b6b8d-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="b6b8d-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b6b8d-125">OUTPUTS</span></span>

### <span data-ttu-id="b6b8d-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="b6b8d-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="b6b8d-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b6b8d-127">NOTES</span></span>

## <span data-ttu-id="b6b8d-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b6b8d-128">RELATED LINKS</span></span>
