---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
ms.openlocfilehash: c0730053dce60dbf556ef00f522aa463ffb26601
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731671"
---
# <span data-ttu-id="f3efd-101">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="f3efd-101">New-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="f3efd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f3efd-102">SYNOPSIS</span></span>
<span data-ttu-id="f3efd-103">Создает новую конфигурацию поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="f3efd-103">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="f3efd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f3efd-104">SYNTAX</span></span>

```
New-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> -ClientId <String> -ClientSecret <String>
 [-AllowedTenants <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f3efd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3efd-105">DESCRIPTION</span></span>
<span data-ttu-id="f3efd-106">Создает новую конфигурацию поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="f3efd-106">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="f3efd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f3efd-107">EXAMPLES</span></span>

### <span data-ttu-id="f3efd-108">Пример 1: Настройка Facebook в качестве поставщика удостоверений для входа на портал разработчика</span><span class="sxs-lookup"><span data-stu-id="f3efd-108">Example 1: Configures Facebook as an identity Provider for Developer Portal Logins</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -ClientId 'sdfsfwerwerw' -ClientSecret 'sdgsdfgfst43tewfewrf'
```

<span data-ttu-id="f3efd-109">Эта команда настраивает удостоверение Facebook как одобренного поставщика удостоверений на портале разработчика службы ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="f3efd-109">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="f3efd-110">Это берет на себя в качестве входных данных ClientId и ClientSecret приложения Facebook.</span><span class="sxs-lookup"><span data-stu-id="f3efd-110">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

## <span data-ttu-id="f3efd-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f3efd-111">PARAMETERS</span></span>

### <span data-ttu-id="f3efd-112">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="f3efd-112">-AllowedTenants</span></span>
<span data-ttu-id="f3efd-113">Список разрешенных клиентов Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="f3efd-113">List of allowed Azure Active Directory Tenants</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3efd-114">-ClientId</span><span class="sxs-lookup"><span data-stu-id="f3efd-114">-ClientId</span></span>
<span data-ttu-id="f3efd-115">Идентификатор клиента приложения в поставщике внешней идентификации.</span><span class="sxs-lookup"><span data-stu-id="f3efd-115">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="f3efd-116">Это идентификатор приложения для входа в Facebook, идентификатор клиента для входа в Google, идентификатор приложения для Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f3efd-116">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="f3efd-117">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="f3efd-117">-ClientSecret</span></span>
<span data-ttu-id="f3efd-118">Секретный ключ клиента приложения во внешнем поставщике удостоверений, используемый для проверки подлинности запроса на вход.</span><span class="sxs-lookup"><span data-stu-id="f3efd-118">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="f3efd-119">Например, это конфиденциальное приложение для входа в Facebook, ключ API для входа в Google, Открытый ключ для Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f3efd-119">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="f3efd-120">-Context</span><span class="sxs-lookup"><span data-stu-id="f3efd-120">-Context</span></span>
<span data-ttu-id="f3efd-121">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="f3efd-121">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="f3efd-122">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="f3efd-122">This parameter is required.</span></span>

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

### <span data-ttu-id="f3efd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3efd-123">-DefaultProfile</span></span>
<span data-ttu-id="f3efd-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f3efd-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3efd-125">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="f3efd-125">-Type</span></span>
<span data-ttu-id="f3efd-126">Идентификатор поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="f3efd-126">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="f3efd-127">Если задано значение, это попытается найти конфигурацию поставщика удостоверений с помощью идентификатора.</span><span class="sxs-lookup"><span data-stu-id="f3efd-127">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="f3efd-128">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="f3efd-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="f3efd-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3efd-129">-Confirm</span></span>
<span data-ttu-id="f3efd-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f3efd-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3efd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3efd-131">-WhatIf</span></span>
<span data-ttu-id="f3efd-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f3efd-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f3efd-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f3efd-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3efd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3efd-134">CommonParameters</span></span>
<span data-ttu-id="f3efd-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f3efd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3efd-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3efd-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3efd-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f3efd-137">INPUTS</span></span>

### <span data-ttu-id="f3efd-138">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f3efd-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f3efd-139">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="f3efd-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="f3efd-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f3efd-140">System.String</span></span>

### <span data-ttu-id="f3efd-141">System. String []</span><span class="sxs-lookup"><span data-stu-id="f3efd-141">System.String[]</span></span>

## <span data-ttu-id="f3efd-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3efd-142">OUTPUTS</span></span>

### <span data-ttu-id="f3efd-143">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="f3efd-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="f3efd-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="f3efd-144">NOTES</span></span>

## <span data-ttu-id="f3efd-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f3efd-145">RELATED LINKS</span></span>

[<span data-ttu-id="f3efd-146">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="f3efd-146">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="f3efd-147">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="f3efd-147">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="f3efd-148">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="f3efd-148">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)
