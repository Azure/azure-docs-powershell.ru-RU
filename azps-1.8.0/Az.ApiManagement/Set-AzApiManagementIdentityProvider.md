---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementIdentityProvider.md
ms.openlocfilehash: f8bc49e4a5b4e8e7fb6285327cf4432cd0561506
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901573"
---
# <span data-ttu-id="eac8d-101">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="eac8d-101">Set-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="eac8d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eac8d-102">SYNOPSIS</span></span>
<span data-ttu-id="eac8d-103">Обновляет конфигурацию существующего поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="eac8d-103">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="eac8d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eac8d-104">SYNTAX</span></span>

```
Set-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-ClientId <String>] [-ClientSecret <String>]
 [-AllowedTenants <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eac8d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eac8d-105">DESCRIPTION</span></span>
<span data-ttu-id="eac8d-106">Обновляет конфигурацию существующего поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="eac8d-106">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="eac8d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eac8d-107">EXAMPLES</span></span>

### <span data-ttu-id="eac8d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="eac8d-108">Example 1</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Set-AzApiManagementIdentityProvider -Context $apimContext -Type Facebook -ClientSecret "updatedSecret" -PassThru
```

<span data-ttu-id="eac8d-109">Командлет обновляет секретный ключ клиента поставщика удостоверений Facebook;</span><span class="sxs-lookup"><span data-stu-id="eac8d-109">The cmdlet updates the Client Secret of the Facebook Identity Provider;</span></span>

## <span data-ttu-id="eac8d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eac8d-110">PARAMETERS</span></span>

### <span data-ttu-id="eac8d-111">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="eac8d-111">-AllowedTenants</span></span>
<span data-ttu-id="eac8d-112">Список разрешенных клиентов Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="eac8d-112">List of allowed Azure Active Directory Tenants.</span></span>

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

### <span data-ttu-id="eac8d-113">-ClientId</span><span class="sxs-lookup"><span data-stu-id="eac8d-113">-ClientId</span></span>
<span data-ttu-id="eac8d-114">Идентификатор клиента приложения в поставщике внешней идентификации.</span><span class="sxs-lookup"><span data-stu-id="eac8d-114">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="eac8d-115">Это идентификатор приложения для входа в Facebook, идентификатор клиента для входа в Google, идентификатор приложения для Microsoft.</span><span class="sxs-lookup"><span data-stu-id="eac8d-115">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="eac8d-116">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="eac8d-116">-ClientSecret</span></span>
<span data-ttu-id="eac8d-117">Секретный ключ клиента приложения во внешнем поставщике удостоверений, используемый для проверки подлинности запроса на вход.</span><span class="sxs-lookup"><span data-stu-id="eac8d-117">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="eac8d-118">Например, это конфиденциальное приложение для входа в Facebook, ключ API для входа в Google, Открытый ключ для Microsoft.</span><span class="sxs-lookup"><span data-stu-id="eac8d-118">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="eac8d-119">-Context</span><span class="sxs-lookup"><span data-stu-id="eac8d-119">-Context</span></span>
<span data-ttu-id="eac8d-120">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="eac8d-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="eac8d-121">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="eac8d-121">This parameter is required.</span></span>

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

### <span data-ttu-id="eac8d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eac8d-122">-DefaultProfile</span></span>
<span data-ttu-id="eac8d-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eac8d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eac8d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eac8d-124">-PassThru</span></span>
<span data-ttu-id="eac8d-125">Указывает на то, что этот командлет возвращает  **PsApiManagementIdentityProvider** , который изменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="eac8d-125">Indicates that this cmdlet returns the  **PsApiManagementIdentityProvider** that this cmdlet modifies.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eac8d-126">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="eac8d-126">-Type</span></span>
<span data-ttu-id="eac8d-127">Идентификатор существующего поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="eac8d-127">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="eac8d-128">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="eac8d-128">This parameter is required.</span></span>

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

### <span data-ttu-id="eac8d-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eac8d-129">-Confirm</span></span>
<span data-ttu-id="eac8d-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="eac8d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eac8d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eac8d-131">-WhatIf</span></span>
<span data-ttu-id="eac8d-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="eac8d-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eac8d-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="eac8d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eac8d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eac8d-134">CommonParameters</span></span>
<span data-ttu-id="eac8d-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eac8d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eac8d-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eac8d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eac8d-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eac8d-137">INPUTS</span></span>

### <span data-ttu-id="eac8d-138">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="eac8d-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="eac8d-139">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="eac8d-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="eac8d-140">System. String</span><span class="sxs-lookup"><span data-stu-id="eac8d-140">System.String</span></span>

### <span data-ttu-id="eac8d-141">System. String []</span><span class="sxs-lookup"><span data-stu-id="eac8d-141">System.String[]</span></span>

### <span data-ttu-id="eac8d-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="eac8d-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="eac8d-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eac8d-143">OUTPUTS</span></span>

### <span data-ttu-id="eac8d-144">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="eac8d-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="eac8d-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="eac8d-145">NOTES</span></span>

## <span data-ttu-id="eac8d-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eac8d-146">RELATED LINKS</span></span>

[<span data-ttu-id="eac8d-147">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="eac8d-147">New-AzApiManagementIdentityProvider</span></span>](./New-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="eac8d-148">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="eac8d-148">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="eac8d-149">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="eac8d-149">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)
