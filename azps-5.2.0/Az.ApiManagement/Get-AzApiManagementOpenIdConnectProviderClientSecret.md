---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementopenidconnectproviderclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProviderClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProviderClientSecret.md
ms.openlocfilehash: dcc66b6d28157ff9d5551e2fdf0cab18f7727828
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322577"
---
# <span data-ttu-id="86e13-101">Get-AzApiManagementOpenIdConnectProviderClientSecret</span><span class="sxs-lookup"><span data-stu-id="86e13-101">Get-AzApiManagementOpenIdConnectProviderClientSecret</span></span>

## <span data-ttu-id="86e13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86e13-102">SYNOPSIS</span></span>
<span data-ttu-id="86e13-103">Получает секрет клиента OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="86e13-103">Gets OpenID Connect provider client secret.</span></span>

## <span data-ttu-id="86e13-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="86e13-104">SYNTAX</span></span>

```
Get-AzApiManagementOpenIdConnectProviderClientSecret -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86e13-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="86e13-105">DESCRIPTION</span></span>
<span data-ttu-id="86e13-106">Получает секрет клиента OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="86e13-106">Gets OpenID Connect provider client secret.</span></span>

## <span data-ttu-id="86e13-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="86e13-107">EXAMPLES</span></span>

### <span data-ttu-id="86e13-108">Пример 1. Получите секрет клиента поставщика с помощью ИД</span><span class="sxs-lookup"><span data-stu-id="86e13-108">Example 1: Get a provider client secret by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProviderClientSecret -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="86e13-109">Эта команда является секретом клиента поставщика ID OICProvider01.</span><span class="sxs-lookup"><span data-stu-id="86e13-109">This command gets a client secret of the provider that has the ID OICProvider01.</span></span>

## <span data-ttu-id="86e13-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86e13-110">PARAMETERS</span></span>

### <span data-ttu-id="86e13-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="86e13-111">-Context</span></span>
<span data-ttu-id="86e13-112">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="86e13-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="86e13-113">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="86e13-113">This parameter is required.</span></span>

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

### <span data-ttu-id="86e13-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86e13-114">-DefaultProfile</span></span>
<span data-ttu-id="86e13-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="86e13-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86e13-116">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="86e13-116">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="86e13-117">Идентификатор поставщика OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="86e13-117">Identifier of a OpenID Connect Provider.</span></span>
<span data-ttu-id="86e13-118">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="86e13-118">This parameter is required.</span></span>

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

### <span data-ttu-id="86e13-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86e13-119">CommonParameters</span></span>
<span data-ttu-id="86e13-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86e13-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86e13-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="86e13-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86e13-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="86e13-122">INPUTS</span></span>

### <span data-ttu-id="86e13-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="86e13-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="86e13-124">System.String</span><span class="sxs-lookup"><span data-stu-id="86e13-124">System.String</span></span>

## <span data-ttu-id="86e13-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="86e13-125">OUTPUTS</span></span>

### <span data-ttu-id="86e13-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="86e13-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="86e13-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="86e13-127">NOTES</span></span>

## <span data-ttu-id="86e13-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="86e13-128">RELATED LINKS</span></span>
