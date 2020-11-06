---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: 76ee402fee2e18d426875340d4eaadda2cc63042
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566346"
---
# <span data-ttu-id="1af49-101">Set-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="1af49-101">Set-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="1af49-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1af49-102">SYNOPSIS</span></span>
<span data-ttu-id="1af49-103">Обновляет конфигурацию существующего поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="1af49-103">Updates the Configuration of an existing Identity Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1af49-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1af49-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-ClientId <String>] [-ClientSecret <String>]
 [-AllowedTenants <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1af49-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1af49-105">DESCRIPTION</span></span>
<span data-ttu-id="1af49-106">Обновляет конфигурацию существующего поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="1af49-106">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="1af49-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1af49-107">EXAMPLES</span></span>

### <span data-ttu-id="1af49-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1af49-108">Example 1</span></span>
```
PS C:\> Set-AzureRmApiManagementIdentityProvider -Context $apimcontext -Type Facebook -ClientSecret "updatedSecret" -PassThru
```

<span data-ttu-id="1af49-109">Командлет обновляет секретный ключ клиента поставщика удостоверений Facebook;</span><span class="sxs-lookup"><span data-stu-id="1af49-109">The cmdlet updates the Client Secret of the Facebook Identity Provider;</span></span>

## <span data-ttu-id="1af49-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1af49-110">PARAMETERS</span></span>

### <span data-ttu-id="1af49-111">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="1af49-111">-AllowedTenants</span></span>
<span data-ttu-id="1af49-112">Список разрешенных клиентов Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1af49-112">List of allowed Azure Active Directory Tenants.</span></span>

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

### <span data-ttu-id="1af49-113">-ClientId</span><span class="sxs-lookup"><span data-stu-id="1af49-113">-ClientId</span></span>
<span data-ttu-id="1af49-114">Идентификатор клиента приложения в поставщике внешней идентификации.</span><span class="sxs-lookup"><span data-stu-id="1af49-114">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="1af49-115">Это идентификатор приложения для входа в Facebook, идентификатор клиента для входа в Google, идентификатор приложения для Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1af49-115">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="1af49-116">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="1af49-116">-ClientSecret</span></span>
<span data-ttu-id="1af49-117">Секретный ключ клиента приложения во внешнем поставщике удостоверений, используемый для проверки подлинности запроса на вход.</span><span class="sxs-lookup"><span data-stu-id="1af49-117">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="1af49-118">Например, это конфиденциальное приложение для входа в Facebook, ключ API для входа в Google, Открытый ключ для Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1af49-118">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="1af49-119">-Context</span><span class="sxs-lookup"><span data-stu-id="1af49-119">-Context</span></span>
<span data-ttu-id="1af49-120">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="1af49-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="1af49-121">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="1af49-121">This parameter is required.</span></span>

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

### <span data-ttu-id="1af49-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1af49-122">-PassThru</span></span>
<span data-ttu-id="1af49-123">Указывает на то, что этот командлет возвращает  **PsApiManagementIdentityProvider** , который изменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="1af49-123">Indicates that this cmdlet returns the  **PsApiManagementIdentityProvider** that this cmdlet modifies.</span></span>


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

### <span data-ttu-id="1af49-124">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="1af49-124">-Type</span></span>
<span data-ttu-id="1af49-125">Идентификатор существующего поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="1af49-125">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="1af49-126">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="1af49-126">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1af49-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1af49-127">-Confirm</span></span>
<span data-ttu-id="1af49-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1af49-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1af49-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1af49-129">-WhatIf</span></span>
<span data-ttu-id="1af49-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1af49-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1af49-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1af49-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1af49-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1af49-132">-DefaultProfile</span></span>
<span data-ttu-id="1af49-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1af49-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1af49-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1af49-134">CommonParameters</span></span>
<span data-ttu-id="1af49-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1af49-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1af49-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1af49-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1af49-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1af49-137">INPUTS</span></span>

## <span data-ttu-id="1af49-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1af49-138">OUTPUTS</span></span>

### <span data-ttu-id="1af49-139">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="1af49-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="1af49-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="1af49-140">NOTES</span></span>

## <span data-ttu-id="1af49-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1af49-141">RELATED LINKS</span></span>

[<span data-ttu-id="1af49-142">New-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="1af49-142">New-AzureRmApiManagementIdentityProvider</span></span>](./New-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="1af49-143">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="1af49-143">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="1af49-144">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="1af49-144">Remove-AzureRmApiManagementIdentityProvider</span></span>](./Remove-AzureRmApiManagementIdentityProvider.md)
