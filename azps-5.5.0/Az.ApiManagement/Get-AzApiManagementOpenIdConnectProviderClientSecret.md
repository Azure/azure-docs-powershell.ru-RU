---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementopenidconnectproviderclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProviderClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProviderClientSecret.md
ms.openlocfilehash: dcc66b6d28157ff9d5551e2fdf0cab18f7727828
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100235385"
---
# <span data-ttu-id="5ffc5-101">Get-AzApiManagementOpenIdConnectProviderClientSecret</span><span class="sxs-lookup"><span data-stu-id="5ffc5-101">Get-AzApiManagementOpenIdConnectProviderClientSecret</span></span>

## <span data-ttu-id="5ffc5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ffc5-102">SYNOPSIS</span></span>
<span data-ttu-id="5ffc5-103">Получает секрет клиента OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="5ffc5-103">Gets OpenID Connect provider client secret.</span></span>

## <span data-ttu-id="5ffc5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5ffc5-104">SYNTAX</span></span>

```
Get-AzApiManagementOpenIdConnectProviderClientSecret -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ffc5-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ffc5-105">DESCRIPTION</span></span>
<span data-ttu-id="5ffc5-106">Получает секрет клиента OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="5ffc5-106">Gets OpenID Connect provider client secret.</span></span>

## <span data-ttu-id="5ffc5-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5ffc5-107">EXAMPLES</span></span>

### <span data-ttu-id="5ffc5-108">Пример 1. Секрет клиента поставщика с помощью ИД</span><span class="sxs-lookup"><span data-stu-id="5ffc5-108">Example 1: Get a provider client secret by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProviderClientSecret -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="5ffc5-109">Эта команда является секретом клиента поставщика ID OICProvider01.</span><span class="sxs-lookup"><span data-stu-id="5ffc5-109">This command gets a client secret of the provider that has the ID OICProvider01.</span></span>

## <span data-ttu-id="5ffc5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ffc5-110">PARAMETERS</span></span>

### <span data-ttu-id="5ffc5-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="5ffc5-111">-Context</span></span>
<span data-ttu-id="5ffc5-112">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="5ffc5-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="5ffc5-113">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="5ffc5-113">This parameter is required.</span></span>

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

### <span data-ttu-id="5ffc5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ffc5-114">-DefaultProfile</span></span>
<span data-ttu-id="5ffc5-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5ffc5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ffc5-116">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="5ffc5-116">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="5ffc5-117">Идентификатор поставщика OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="5ffc5-117">Identifier of a OpenID Connect Provider.</span></span>
<span data-ttu-id="5ffc5-118">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="5ffc5-118">This parameter is required.</span></span>

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

### <span data-ttu-id="5ffc5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ffc5-119">CommonParameters</span></span>
<span data-ttu-id="5ffc5-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ffc5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ffc5-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5ffc5-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ffc5-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5ffc5-122">INPUTS</span></span>

### <span data-ttu-id="5ffc5-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5ffc5-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5ffc5-124">System.String</span><span class="sxs-lookup"><span data-stu-id="5ffc5-124">System.String</span></span>

## <span data-ttu-id="5ffc5-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5ffc5-125">OUTPUTS</span></span>

### <span data-ttu-id="5ffc5-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="5ffc5-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="5ffc5-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5ffc5-127">NOTES</span></span>

## <span data-ttu-id="5ffc5-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5ffc5-128">RELATED LINKS</span></span>
