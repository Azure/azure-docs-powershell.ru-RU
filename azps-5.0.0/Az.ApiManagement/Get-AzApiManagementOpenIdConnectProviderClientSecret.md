---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementopenidconnectproviderclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProviderClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProviderClientSecret.md
ms.openlocfilehash: dcc66b6d28157ff9d5551e2fdf0cab18f7727828
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246942"
---
# <span data-ttu-id="2dc3a-101">Get-AzApiManagementOpenIdConnectProviderClientSecret</span><span class="sxs-lookup"><span data-stu-id="2dc3a-101">Get-AzApiManagementOpenIdConnectProviderClientSecret</span></span>

## <span data-ttu-id="2dc3a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2dc3a-102">SYNOPSIS</span></span>
<span data-ttu-id="2dc3a-103">Возвращает секрет клиента поставщика подключений OpenID.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-103">Gets OpenID Connect provider client secret.</span></span>

## <span data-ttu-id="2dc3a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2dc3a-104">SYNTAX</span></span>

```
Get-AzApiManagementOpenIdConnectProviderClientSecret -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2dc3a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2dc3a-105">DESCRIPTION</span></span>
<span data-ttu-id="2dc3a-106">Возвращает секрет клиента поставщика подключений OpenID.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-106">Gets OpenID Connect provider client secret.</span></span>

## <span data-ttu-id="2dc3a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2dc3a-107">EXAMPLES</span></span>

### <span data-ttu-id="2dc3a-108">Пример 1: получение секрета клиента поставщика с помощью идентификатора</span><span class="sxs-lookup"><span data-stu-id="2dc3a-108">Example 1: Get a provider client secret by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProviderClientSecret -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="2dc3a-109">Эта команда получает секретный ключ клиента поставщика с ИД OICProvider01.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-109">This command gets a client secret of the provider that has the ID OICProvider01.</span></span>

## <span data-ttu-id="2dc3a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2dc3a-110">PARAMETERS</span></span>

### <span data-ttu-id="2dc3a-111">-Context</span><span class="sxs-lookup"><span data-stu-id="2dc3a-111">-Context</span></span>
<span data-ttu-id="2dc3a-112">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2dc3a-113">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-113">This parameter is required.</span></span>

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

### <span data-ttu-id="2dc3a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dc3a-114">-DefaultProfile</span></span>
<span data-ttu-id="2dc3a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2dc3a-116">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="2dc3a-116">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="2dc3a-117">Идентификатор поставщика OpenID подключения.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-117">Identifier of a OpenID Connect Provider.</span></span>
<span data-ttu-id="2dc3a-118">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-118">This parameter is required.</span></span>

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

### <span data-ttu-id="2dc3a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dc3a-119">CommonParameters</span></span>
<span data-ttu-id="2dc3a-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dc3a-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2dc3a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dc3a-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2dc3a-122">INPUTS</span></span>

### <span data-ttu-id="2dc3a-123">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2dc3a-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2dc3a-124">System. String</span><span class="sxs-lookup"><span data-stu-id="2dc3a-124">System.String</span></span>

## <span data-ttu-id="2dc3a-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2dc3a-125">OUTPUTS</span></span>

### <span data-ttu-id="2dc3a-126">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="2dc3a-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="2dc3a-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="2dc3a-127">NOTES</span></span>

## <span data-ttu-id="2dc3a-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2dc3a-128">RELATED LINKS</span></span>
