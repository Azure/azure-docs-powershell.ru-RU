---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityproviderclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProviderClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProviderClientSecret.md
ms.openlocfilehash: d75d385bc158e0855601d3432dff79b2e4339f2f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94315401"
---
# <span data-ttu-id="a0083-101">Get-AzApiManagementIdentityProviderClientSecret</span><span class="sxs-lookup"><span data-stu-id="a0083-101">Get-AzApiManagementIdentityProviderClientSecret</span></span>

## <span data-ttu-id="a0083-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a0083-102">SYNOPSIS</span></span>
<span data-ttu-id="a0083-103">Получите секрет клиента поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="a0083-103">Get the identity provider client secret.</span></span>

## <span data-ttu-id="a0083-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a0083-104">SYNTAX</span></span>

```
Get-AzApiManagementIdentityProviderClientSecret -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0083-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0083-105">DESCRIPTION</span></span>
<span data-ttu-id="a0083-106">Получите секрет клиента поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="a0083-106">Get the identity provider client secret.</span></span>

## <span data-ttu-id="a0083-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a0083-107">EXAMPLES</span></span>

### <span data-ttu-id="a0083-108">Пример 1: получение секрета клиента для поставщика удостоверений типа AAD</span><span class="sxs-lookup"><span data-stu-id="a0083-108">Example 1: Get the client secret of AAD Type Identity Provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Get-AzApiManagementIdentityProviderClientSecret -Context $apimContext -Type Aad
```

<span data-ttu-id="a0083-109">Получает секретный ключ клиента конфигурации поставщика удостоверений Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a0083-109">Gets the client secret of the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="a0083-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a0083-110">PARAMETERS</span></span>

### <span data-ttu-id="a0083-111">-Context</span><span class="sxs-lookup"><span data-stu-id="a0083-111">-Context</span></span>
<span data-ttu-id="a0083-112">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="a0083-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a0083-113">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="a0083-113">This parameter is required.</span></span>

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

### <span data-ttu-id="a0083-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0083-114">-DefaultProfile</span></span>
<span data-ttu-id="a0083-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a0083-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0083-116">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="a0083-116">-Type</span></span>
<span data-ttu-id="a0083-117">Идентификатор поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="a0083-117">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="a0083-118">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="a0083-118">This parameter is required.</span></span>

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

### <span data-ttu-id="a0083-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0083-119">CommonParameters</span></span>
<span data-ttu-id="a0083-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a0083-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0083-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0083-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0083-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a0083-122">INPUTS</span></span>

### <span data-ttu-id="a0083-123">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a0083-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a0083-124">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="a0083-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="a0083-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0083-125">OUTPUTS</span></span>

### <span data-ttu-id="a0083-126">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="a0083-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="a0083-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="a0083-127">NOTES</span></span>

## <span data-ttu-id="a0083-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a0083-128">RELATED LINKS</span></span>
