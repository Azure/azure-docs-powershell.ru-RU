---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
ms.openlocfilehash: b267fc854127c1cb098481ac483a7572c8b2e12f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079896"
---
# <span data-ttu-id="4e25c-101">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="4e25c-101">Get-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="4e25c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4e25c-102">SYNOPSIS</span></span>
<span data-ttu-id="4e25c-103">Получение сведений о конфигурации поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="4e25c-103">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="4e25c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4e25c-104">SYNTAX</span></span>

### <span data-ttu-id="4e25c-105">AllIdentityProviders (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4e25c-105">AllIdentityProviders (Default)</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e25c-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="4e25c-106">IdentityProviderByType</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e25c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e25c-107">DESCRIPTION</span></span>
<span data-ttu-id="4e25c-108">Получение сведений о конфигурации поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="4e25c-108">Get the identity provider configuration details.</span></span>
<span data-ttu-id="4e25c-109">ClientSecret не будет включаться в данные результата.</span><span class="sxs-lookup"><span data-stu-id="4e25c-109">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="4e25c-110">Чтобы получить секрет клиента, используйте **Get-AzApiManagementIdentityProviderClientSecret**.</span><span class="sxs-lookup"><span data-stu-id="4e25c-110">To get client secret, use **Get-AzApiManagementIdentityProviderClientSecret**.</span></span>

## <span data-ttu-id="4e25c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4e25c-111">EXAMPLES</span></span>

### <span data-ttu-id="4e25c-112">Пример 1: получение всех поставщиков удостоверений</span><span class="sxs-lookup"><span data-stu-id="4e25c-112">Example 1: Get all Identity Providers</span></span>

```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementIdentityProvider -Context $apimContext
```

<span data-ttu-id="4e25c-113">Получение всех конфигураций поставщика удостоверений в службе.</span><span class="sxs-lookup"><span data-stu-id="4e25c-113">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="4e25c-114">Пример 2: получение поставщика удостоверений типа AAD</span><span class="sxs-lookup"><span data-stu-id="4e25c-114">Example 2: Get the AAD Type Identity Provider</span></span>
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

<span data-ttu-id="4e25c-115">Возвращает конфигурацию поставщика удостоверений Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4e25c-115">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

### <span data-ttu-id="4e25c-116">Пример 3: получение поставщика удостоверений типа AAD B2C</span><span class="sxs-lookup"><span data-stu-id="4e25c-116">Example 3: Get the AAD B2C Type Identity Provider</span></span>
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

<span data-ttu-id="4e25c-117">Возвращает конфигурацию поставщика удостоверений Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4e25c-117">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="4e25c-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4e25c-118">PARAMETERS</span></span>

### <span data-ttu-id="4e25c-119">-Context</span><span class="sxs-lookup"><span data-stu-id="4e25c-119">-Context</span></span>
<span data-ttu-id="4e25c-120">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="4e25c-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="4e25c-121">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="4e25c-121">This parameter is required.</span></span>

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

### <span data-ttu-id="4e25c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e25c-122">-DefaultProfile</span></span>
<span data-ttu-id="4e25c-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e25c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e25c-124">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="4e25c-124">-Type</span></span>
<span data-ttu-id="4e25c-125">Идентификатор поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="4e25c-125">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="4e25c-126">Если задано значение, это попытается найти конфигурацию поставщика удостоверений с помощью идентификатора.</span><span class="sxs-lookup"><span data-stu-id="4e25c-126">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="4e25c-127">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="4e25c-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="4e25c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e25c-128">CommonParameters</span></span>
<span data-ttu-id="4e25c-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4e25c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e25c-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e25c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e25c-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4e25c-131">INPUTS</span></span>

### <span data-ttu-id="4e25c-132">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4e25c-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4e25c-133">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="4e25c-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="4e25c-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e25c-134">OUTPUTS</span></span>

### <span data-ttu-id="4e25c-135">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="4e25c-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="4e25c-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="4e25c-136">NOTES</span></span>

## <span data-ttu-id="4e25c-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e25c-137">RELATED LINKS</span></span>