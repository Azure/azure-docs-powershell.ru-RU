---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
ms.openlocfilehash: 75525d3c77c3e2113c0e3cff5a7741ab916d7485
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066403"
---
# <span data-ttu-id="a2b5f-101">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="a2b5f-101">Get-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="a2b5f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a2b5f-102">SYNOPSIS</span></span>
<span data-ttu-id="a2b5f-103">Получение сведений о конфигурации поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-103">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="a2b5f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a2b5f-104">SYNTAX</span></span>

### <span data-ttu-id="a2b5f-105">AllIdentityProviders (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a2b5f-105">AllIdentityProviders (Default)</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2b5f-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="a2b5f-106">IdentityProviderByType</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2b5f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2b5f-107">DESCRIPTION</span></span>
<span data-ttu-id="a2b5f-108">Получение сведений о конфигурации поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-108">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="a2b5f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a2b5f-109">EXAMPLES</span></span>

### <span data-ttu-id="a2b5f-110">Пример 1: получение всех поставщиков удостоверений</span><span class="sxs-lookup"><span data-stu-id="a2b5f-110">Example 1: Get all Identity Providers</span></span>

```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementIdentityProvider -Context $apimContext
```

<span data-ttu-id="a2b5f-111">Получение всех конфигураций поставщика удостоверений в службе.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-111">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="a2b5f-112">Пример 2: получение поставщика удостоверений типа AAD</span><span class="sxs-lookup"><span data-stu-id="a2b5f-112">Example 2: Get the AAD Type Identity Provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Get-AzApiManagementIdentityProvider -Context $apimContext -Type Aad


Type                     : Aad
ClientId                 : aaa
ClientSecret             : xxxxx
AllowedTenants           : {contosotest.onmicrosoft.com}
Authority                : login.microsoftonline.com
SignupPolicyName         :
SigninPolicyName         :
ProfileEditingPolicyName :
PasswordResetPolicyName  :
SigninTenant             :
Id                       : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/identityProviders/Aad
ResourceGroupName        : Api-Default-West-US
ServiceName              : contoso
```

<span data-ttu-id="a2b5f-113">Возвращает конфигурацию поставщика удостоверений Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-113">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

### <span data-ttu-id="a2b5f-114">Пример 3: получение поставщика удостоверений типа AAD B2C</span><span class="sxs-lookup"><span data-stu-id="a2b5f-114">Example 3: Get the AAD B2C Type Identity Provider</span></span>
```powershell
PS C:\>$context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Get-AzApiManagementIdentityProvider -Context $context -Type AadB2C


Type                     : AadB2C
ClientId                 : f02dafe2-b8b8-48ec-a38e-27e5c16c51e5
ClientSecret             : xxxxxx
AllowedTenants           : {contosoaadb2c.onmicrosoft.com}
Authority                : login.microsoftonline.com
SignupPolicyName         : B2C_1_policy-signup
SigninPolicyName         : B2C_1_policy-signin
ProfileEditingPolicyName :
PasswordResetPolicyName  :
SigninTenant             : contosoaadb2c.onmicrosoft.com
Id                       : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/identityProviders/AadB2C
ResourceGroupName        : Api-Default-West-US
ServiceName              : contoso
```

<span data-ttu-id="a2b5f-115">Возвращает конфигурацию поставщика удостоверений Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-115">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="a2b5f-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a2b5f-116">PARAMETERS</span></span>

### <span data-ttu-id="a2b5f-117">-Context</span><span class="sxs-lookup"><span data-stu-id="a2b5f-117">-Context</span></span>
<span data-ttu-id="a2b5f-118">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a2b5f-119">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-119">This parameter is required.</span></span>

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

### <span data-ttu-id="a2b5f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2b5f-120">-DefaultProfile</span></span>
<span data-ttu-id="a2b5f-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2b5f-122">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="a2b5f-122">-Type</span></span>
<span data-ttu-id="a2b5f-123">Идентификатор поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-123">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="a2b5f-124">Если задано значение, это попытается найти конфигурацию поставщика удостоверений с помощью идентификатора.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-124">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="a2b5f-125">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-125">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: IdentityProviderByType
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2b5f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2b5f-126">CommonParameters</span></span>
<span data-ttu-id="a2b5f-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2b5f-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2b5f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2b5f-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a2b5f-129">INPUTS</span></span>

### <span data-ttu-id="a2b5f-130">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a2b5f-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a2b5f-131">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="a2b5f-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="a2b5f-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2b5f-132">OUTPUTS</span></span>

### <span data-ttu-id="a2b5f-133">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="a2b5f-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="a2b5f-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="a2b5f-134">NOTES</span></span>

## <span data-ttu-id="a2b5f-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a2b5f-135">RELATED LINKS</span></span>
